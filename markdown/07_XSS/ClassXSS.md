# XSS 基礎防護

## 什麼是 XSS？

XSS（Cross-Site Scripting）是一種網頁安全漏洞，允許攻擊者在網頁中注入惡意的腳本代碼（通常是 JavaScript），以便在用戶的瀏覽器中執行。這種攻擊可以讓攻擊者竊取用戶的敏感資料、控制用戶的瀏覽器或執行其他惡意行為。

## 容易發生的環境

* 網頁沒有正確地驗證用戶的輸入資料
* 網頁使用不安全的方法來處理用戶的輸入資料
* 網頁沒有設置適當的安全 Header（Security Header）

## 常見 XSS 攻擊類型

* Stored XSS：
  * 攻擊者將惡意代碼儲存到網頁的資料庫中，然後當用戶訪問網頁時，惡意代碼會被執行。

  ``` html
  <script>alert('XSS')</script>
  ```

* Reflected XSS：
  * 攻擊者將惡意代碼包含在網頁的 URL 中，然後當用戶訪問網頁時，惡意代碼會被執行。
  `http://example.com/search?q=<script>alert('XSS')</script>`

* DOM-based XSS：
  * 攻擊者將惡意代碼注入網頁的 DOM 中，然後當用戶互動網頁時，惡意代碼會被執行。

  ``` html
  <input type="text" id="username" value="<script>alert('XSS')</script>">
  ```

## 防範措施

* 驗證用戶的輸入資料
  * 使用白名單（Whitelist）來驗證用戶的輸入資料，只允許特定的字符和格式。
  * 例如：驗證用戶的姓名輸入，只允許英文字母、空格和特殊字符（如 -、.）。

    ``` javascript
    function validateName(name) {
        const whitelist = /^[a-zA-Z\s\-\.]+$/;
        return whitelist.test(name);
    }
    ```

  * PHP 可使用 `htmlspecialchars()` 函數將用戶的輸入資料轉換為安全的 HTML 代碼，避免 XSS 攻擊。

* 使用安全的方法來處理用戶的輸入資料
  * 使用 HTML 編碼（HTML Encoding）來將用戶的輸入資料轉換為安全的 HTML 代碼。
  * 例如：將用戶的輸入資料轉換為 HTML 代碼，避免 XSS 攻擊。

    ``` javascript
    function encodeHtml(input) {
    return input.replace(/&/g, '&amp;')
                .replace(/</g, '&lt;')
                .replace(/>/g, '&gt;')
                .replace(/"/g, '&quot;')
                .replace(/'/g, '&#x27;');
    }
    ```

  * PHP 可使用 `htmlspecialchars()` 函數將用戶的輸入資料轉換為安全的 HTML 代碼，避免 XSS 攻擊。

* 設置適當的 Security Header
  * 設置 Content-Security-Policy (CSP) 首部來限制網頁中可以執行的腳本代碼。
  * 例如：設置 CSP 首部來限制網頁中只能執行來自自己網站的腳本代碼。

    ``` http
    Content-Security-Policy: script-src 'self';
    ```

* 使用內容安全政策（Content Security Policy）來限制網頁中可以執行的腳本代碼。
  * 設置 CSP 政策來限制網頁中可以執行的腳本代碼。
  * 例如：設置 CSP 政策來限制網頁中只能執行來自自己網站的腳本代碼，並且禁止執行內嵌腳本代碼

    ``` http
    Content-Security-Policy:
    script-src 'self';
    object-src 'none';
    frame-src 'none';
    child-src 'none';
    plugin-types application/pdf;
    ```

## 實作