# CSRF

## 什麼是 CSRF ？

CSRF是一種攻擊手法，攻擊者透過誘騙用戶點擊某個連結或按鈕，從而在用戶不知情的情況下，向受害網站發送請求，執行某些操作。

## CSRF攻擊的原理

1. 攻擊者在自己的網站上建立一個惡意連結或按鈕，當用戶點擊時，會向受害網站發送請求。
2. 受害網站收到請求後，會執行相應的操作，例如：刪除用戶資料、修改用戶密碼等。
3. 攻擊者可以透過這種方式，執行任意的操作，從而達到攻擊的目的。

## CSRF攻擊的類型

1. GET型CSRF攻擊：攻擊者在自己的網站上建立一個惡意連結，當用戶點擊時，會向受害網站發送GET請求。
2. POST型CSRF攻擊：攻擊者在自己的網站上建立一個惡意表單，當用戶提交表單時，會向受害網站發送POST請求。

## 預防CSRF攻擊的方法

1. Token驗證：在用戶的請求中加入一個隨機的Token，當用戶提交請求時，驗證Token是否正確。
2. Header驗證：在用戶的請求中加入一個特定的Header，當用戶提交請求時，驗證Header是否正確。
3. 雙重提交Cookie：在用戶的請求中加入一個Cookie，當用戶提交請求時，驗證Cookie是否正確。

## PHP 的 CSRF 範例

產生 Token

``` php
function generate_token() {
    $token = bin2hex(random_bytes(32));
    $_SESSION['token'] = $token;
    return $token;
}
```

驗證 Token

``` php
function verify_token($token) {
    if ($token !== $_SESSION['token']) {
        throw new Exception('CSRF 攻擊');
    }
}
```

表單範例

``` html
<form action="/example" method="post">
    <input type="hidden" name="token" value="<?= generate_token() ?>">
    <!-- 表單內容 -->
    <button type="submit">提交</button>
</form>
```

處理表單  Submit

``` php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $token = $_POST['token'];
    verify_token($token);
    // 執行操作
    echo '操作成功';
}
```

使用 Header 驗證

``` php
function verify_header() {
    $header = $_SERVER['HTTP_X_CSRF_TOKEN'];
    if ($header !== $_SESSION['token']) {
        throw new Exception('CSRF 攻擊');
    }
}
```

示例表單（使用 Header 驗證）

``` php
<form action="/example" method="post">
    <!-- 表單內容 -->
    <button type="submit">提交</button>
</form>
```

處理表單提交（使用 Header 驗證）

``` php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    verify_header();
    // 執行操作
    echo '操作成功';
}
```

使用雙重提交 Cookie

``` php
function verify_cookie() {
    $cookie = $_COOKIE['csrf_token'];
    if ($cookie !== $_SESSION['token']) {
        throw new Exception('CSRF 攻擊');
    }
}
```

表單範例（使用雙重提交 Cookie）

``` html
<form action="/example" method="post">
    <!-- 表單內容 -->
    <button type="submit">提交</button>
</form>
```

處理表單Submit（使用雙重提交 Cookie）

``` php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    verify_cookie();
    // 執行操作
    echo '操作成功';
}
```

GET 型 CSRF 攻擊

``` bash
curl -X GET \
  http://example.com/vulnerable-page \
  -H 'Cookie: session_id=abc123' \
  -H 'Referer: http://attacker.com'
```

POST 型 CSRF 攻擊

``` bash
curl -X POST \
  http://example.com/vulnerable-page \
  -H 'Cookie: session_id=abc123' \
  -H 'Referer: http://attacker.com' \
  -d 'username=admin&password=123456'
```

使用 Token 驗證的 CSRF 攻擊

``` bash
curl -X POST \
  http://example.com/vulnerable-page \
  -H 'Cookie: session_id=abc123' \
  -H 'Referer: http://attacker.com' \
  -d 'username=admin&password=123456&token=abc123'
```

使用 Header 驗證的 CSRF 攻擊

``` bash
curl -X POST \
  http://example.com/vulnerable-page \
  -H 'Cookie: session_id=abc123' \
  -H 'Referer: http://attacker.com' \
  -H 'X-CSRF-Token: abc123' \
  -d 'username=admin&password=123456'
```

使用雙重提交 Cookie 的 CSRF 攻擊

``` bash
curl -X POST \
  http://example.com/vulnerable-page \
  -H 'Cookie: session_id=abc123; csrf_token=abc123' \
  -H 'Referer: http://attacker.com' \
  -d 'username=admin&password=123456'
```