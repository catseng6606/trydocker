# 進階網頁設計

* Jquery
* Bootstrap

## 什麼是 Jquery?
* 是一個 JavaScript 函式庫，能夠簡化 JavaScript 的使用
* 提供了許多實用的方法，能夠讓開發者快速地產生網頁動態效果

## 快速使用 Jquery

你可以在 HTML 文件中使用 `<script>` 標籤引用 CDN。例如，引用 jQuery 的 CDN：

``` html
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
```

## Jquery 入門範例：

``` html
<!DOCTYPE html>
<html>
<head>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
  <button id="myButton">點擊我</button>
  <div id="myDiv">Hello World!</div>

  <script>
    $(document).ready(function() {
      $('#myButton').click(function() {
        $('#myDiv').hide();
      });
    });
  </script>
</body>
</html>
```

## 什麼是 Bootstrap？
* 是一個前端 Framework
* 讓設計網頁更加簡單、快速

## 快速使用 Bootstrap

你可以在 HTML 文件中使用 `<link>` 標籤引用 Bootstrap 的 CSS 文件，和 `<script>` 標籤引用 Bootstrap 的 JavaScript 文件。例如：

``` html
<!-- 引用 Bootstrap 的 CSS 文件 -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css">

<!-- 引用 Bootstrap 的 JavaScript 文件 -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
```

## Bootstrap 入門範例

``` html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css">
</head>
<body>
  <div class="container">
    <h1 class="display-1">Hello World!</h1>
    <p class="lead">這是一個 Bootstrap 的入門範例。</p>
    <button class="btn btn-primary">點擊我</button>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## Bootstrap 的主要類別

以下是一些 Bootstrap 的主要類別：

* `.container`: 容器類別，用于包裹網頁的內容。
* `.display-1`: 標題類別，用于顯示大標題。
* `.lead`: 段落類別，用于顯示重要的段落。
* `.btn`: 按鈕類別，用于顯示按鈕。
* `.btn-primary`: 按鈕類別，用于顯示主要按鈕。

這些類別可以幫助你快速設計出美觀的網頁。

## 實作 Jquery + Bootstrap