# 網頁技術基礎課程

## 有哪些基礎技術？

* HTML （ Hypertext Markup Language ）
* CSS （ Cascading Style Sheets ）
* JavaScript
* Bootstrap
* 其他：Jquery、Vue、Angular、React......

## 有哪些工具可以使用？

* Visual Studio Code [https://code.visualstudio.com/](https://code.visualstudio.com/)
* WebStorm [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/)
* Atom [https://atom-editor.cc/](https://atom-editor.cc/)
* Sublime Text [https://www.sublimetext.com/](https://www.sublimetext.com/)

## 有哪些 AI 輔助工具可以使用（個人觀點）

* Codeium 
* ChatGPT 
* Qodo Gen
* Google Gemini

## 什麼是 HTML?

* HTML係用來告訴瀏覽器如何呈現網頁的標記語言
* 目前版本 HTML5
* 主要組成（元素）：開始標籤 &lt;h1&gt;、結束標籤 &lt;/h1&gt;、屬性
* 巢狀元素：

  ```HTML
  <p>My cat is <strong>very</strong> grumpy.</p>
  ```

* 空元素：&lt;div /&gt;

## 安裝開發工具 VS Code

1. 安裝 Visual Studio Code
2. 安裝套件：
   1. 中文套件
   2. Live Server
   3. Live Share
   4. 輔助撰寫套件（提示、標籤自動完成等）
   5. 美化套件（排版、程式碼閱讀等）
   6. 版本控制（Git、GitLen等）
   7. AI 工具 （Codeium）

## 實作 1 （Hello.html）

1. 使用 VSCODE 新增 hello.html（快速鍵：!）
2. 使用 Live Server 觀看結果 （右下角 Go Live）

## `<!DOCTYPE html>`

`<!DOCTYPE html>` 是 HTML 文件的文件類型宣告（Document Type Declaration，DTD）。它告訴瀏覽器這是一個 HTML 文件，並且指定了文件的版本。

在 HTML5 中，`<!DOCTYPE html>` 是唯一需要的 DTD 宣告。它告訴瀏覽器這是一個 HTML5 文件，並且啟用了 HTML5 的功能。

## `<html>`

* `<html>` 是 HTML 文件的根元素（Root Element），它包裹了整個 HTML 文件的內容。
* `lang` 屬性是 `<html>` 元素的一個屬性，用於指定 HTML 文件的語言，例如 `en` 代表英語， `zh-TW` 代表繁體中文， `ja` 代表日語等。

## `<head>`

`<head>` 是 HTML 文件的 Head Element，它包含了文件的 metadata，例如文件的 TITLE、文字編碼、CSS 樣式表和JAVA SCRIPTS等。

```HTML
<head>
  <title>文件標題</title>
  <meta charset="UTF-8">
  <meta name="description" content="文件描述">
  <link rel="stylesheet" href="style.css">
  <script src="script.js"></script>
</head>
```

## `<body>`

* `<h1>-<h6>`：標題元素
* `<p>`：段落元素
* `<img>`：圖片元素
* `<table>`：表格元素
* `<form>`：表單元素
* `<div>`：區塊元素
* `<span>`：內嵌元素

## 實作 2 (body.html)

## 什麼是 HTML5 ？

HTML5 是 HTML 的最新版本，於 2014 年正式發布。相較於舊版 HTML，HTML5 有許多新的特性和改進。

## HTML5 新特性

1. 語義化標籤 （Semantic）：TML5 引入了許多新的語義化標籤，例如 `<header>`、`<nav>`、`<main>`、`<section>`、`<article>`、`<aside>`、`<footer>` 等，取代了舊版 HTML 中的 `<div>` 和 `<span>` 標籤。
2. 多媒體支援：例如：`<video>`、`<audio>`
3. 離線存取
4. 地理位置
5. 本地儲存與本地 SQL DataBase

## HTML5 主要新 TAGS

1. `<header>`：定義文件或區塊的標題。
2. `<nav>`：定義文件或區塊的導航欄。
3. `<main>`：定義文件的主要內容區域。
4. `<section>`：定義文件的一個區塊或章節。
5. `<article>`：定義文件的一篇文章或內容。
6. `<aside>`：定義文件的一個補充內容或側欄。
7. `<footer>`：定義文件或區塊的底部信息。
8. `<video>`：定義影片內容。
9. `<audio>`：定義音頻內容。
10. `<canvas>`：定義繪圖區域。



## 實作 3 (html5.html)

``` HTML
<!DOCTYPE html>
<html>
<head>
  <title>HTML5 範例</title>
</head>
<body>
  <header>
    <h1>網頁標題</h1>
  </header>
  <nav>
    <ul>
      <li><a href="#">首頁</a></li>
      <li><a href="#">關於我們</a></li>
    </ul>
  </nav>
  <main>
    <section>
      <h2>文章標題</h2>
      <p>文章內容</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2023 網頁作者</p>
  </footer>
</body>
</html>
```

## 實作：使用 Emmet 快速鍵 (Emmet.html)

## 實作 4 (ai.html)

## 參考資料

1. [https://developer.mozilla.org/zh-TW/docs/Learn_web_development](https://developer.mozilla.org/zh-TW/docs/Learn_web_development)
2. [https://ithelp.ithome.com.tw/users/20112550/ironman/2072](https://ithelp.ithome.com.tw/users/20112550/ironman/2072)
