# CSS

## 什麼是 CSS？

CSS（Cascading Style Sheets）是一種用於控制網頁外觀和佈局的樣式的語言。它允許我們定義網頁元素的樣式、佈局和動畫效果。

CSS 的主要功能包括：

* 控制網頁元素的外觀，例如顏色、字體、大小等
* 定義網頁元素的佈局，例如位置、寬度、高度等
* 創建動畫效果和交互效果
* 控制網頁的樣式

CSS 的基本語法包括：

* 選擇器（Selector）：用於選擇網頁元素
* 屬性（Property）：用於定義網頁元素的樣式
* 值（Value）：用於指定屬性的值

CSS 最新版本：CSS3

## 三種 CSS 類型

1. 內嵌樣式表（Inline Style）

``` HTML
<p style="color: red; font-size: 24px;">這是一個內嵌樣式表的例子</p>
```

2. 內部樣式表（Internal Style）

``` HTML
<head>
  <style>
    h1 {
      color: blue;
      font-size: 36px;
    }
  </style>
</head>
<body>
  <h1>這是一個內部樣式表的例子</h1>
</body>
```

3. 外部樣式表（External Style）

``` HTML
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <h1>這是一個外部樣式表的例子</h1>
</body>
```

## 實作

1. 新增 CSS.html (使用驚嘆號！)
2. 新增 `<h1>Hello Inline Style</h1>`、`<h2>Hello Internal Style</h2>`、`<h3>Hello External Style</h3>`
3. 新增 styles.css

``` HTML
/* style.css */
h3 {
  color: green;
  font-size: 48px;
}
```

4. 完成 `<h1>`、`<h2>`、`<h3>` 套用 CSS

## 常用文字屬性

* color: 指定文字顏色
* font-size: 指定文字大小
* font-family: 指定文字字體
* font-weight: 指定文字粗細
* text-align: 指定文字對齊方式
* text-decoration: 指定文字裝飾（例如下劃線、刪除線等）

## 常用邊框屬性

* border-width: 指定邊框寬度
* border-style: 指定邊框樣式（例如實線、虛線等）
* border-color: 指定邊框顏色
* border-radius: 指定邊框圓角

## 常用尺寸屬性

* width: 指定元素寬度
* height: 指定元素高度
* max-width: 指定元素最大寬度
* max-height: 指定元素最大高度
* min-width: 指定元素最小寬度
* min-height: 指定元素最小高度

## 常用定位屬性

* position: 指定元素定位方式（例如相對定位、絕對定位等）
* top: 指定元素頂部距離
* right: 指定元素右邊距離
* bottom: 指定元素底部距離
* left: 指定元素左邊距離
* z-index: 指定元素堆疊順序

## 常用顯示屬性

* display: 指定元素顯示方式（例如塊級元素、內嵌元素等）
* visibility: 指定元素可見性
* opacity: 指定元素透明度

## 常用其他屬性

* margin: 指定元素外邊距
* padding: 指定元素內邊距
* overflow: 指定元素溢出內容處理方式
* cursor: 指定鼠標游標樣式