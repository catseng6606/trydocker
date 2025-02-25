## 什麼是 Java Script？

JavaScript是一種高級的、動態的、基於物件的腳本語言，主要用於網頁開發。它可以用來創建動態網頁、網頁應用程序和移動應用程序。

* JavaScript 是一種腳本語言，可以直接執行，不需要編譯。
* JavaScript 可以動態地修改網頁的內容和樣式。
* JavaScript 可以用來串接後端的 Server 端應用程式和API。

## JavaScript的基本語法：變數

* 變數: JavaScript的變數可以用來存儲數據。
* 變數的宣告: 可以使用 let、const 或 var 來宣告變數。
* 變數的命名: 變數的命名必須遵守一定的規則，例如不能使用關鍵字、不能以數字開頭等。

```JS
let name = 'John Doe';
const age = 30;
var occupation = 'Software Engineer';
```

## JavaScript的基本語法：資料類型

* 資料類型: JavaScript有多種數據類型，包括數字、字符串、布爾值、物件和陣列。
* 數字: 可以使用 number 來宣告數字。
* 字串: 可以使用 string 來宣告字串變數。
* 布林值: 可以使用 boolean 來宣告布林值變數。
* 物件: 可以使用 {} 來宣告物件變數。
* 陣列: 可以使用 [] 來宣告陣列變數。

```JS
let num = 42;
let str = 'Hello World!';
let bool = true;
let obj = { name: 'John Doe', age: 30 };
let arr = [1, 2, 3, 4, 5];
```

## JavaScript的基本語法：運算子

* 運算子: JavaScript有多種運算子，可以用來執行算術、比較和邏輯運算。
* 算術運算子: 可以使用 +、-、*、/ 等來執行算術運算。
* 比較運算子: 可以使用 ==、!=、>、< 等來執行比較運算。
* 邏輯運算子: 可以使用 &&、||、! 等來執行邏輯運算。

``` JS
let result = 2 + 3; // 5
let isEqual = 2 == 3; // false
let isGreater = 2 > 3; // false
let isValid = true && false; // false
```

## JavaScript的基本語法：流程控制

* 流程控制: JavaScript有多種控制結構，可以用來控制程式的流程。
* if...else: 可以使用 if 和 else 來執行條件判斷。
* switch: 可以使用 switch 來執行多重條件判斷。
* for: 可以使用 for 來執行迴圈。
* while: 可以使用 while 來執行迴圈。

``` JS
let age = 30;
if (age > 18) {
  console.log('您已經成年!');
} else {
  console.log('您還未成年!');
}

let color = 'red';
switch (color) {
  case 'red':
    console.log('紅色!');
    break;
  case 'green':
    console.log('綠色!');
    break;
  default:
    console.log('其他顏色!');
}

for (let i = 0; i < 5; i++) {
  console.log(i);
}

let j = 0;
while (j < 5) {
  console.log(j);
  j++;
}
```

## JavaScript的基本語法：函數

* 函數: JavaScript的函數可以用來封裝程式碼和重複使用。
* 函數的宣告: 可以使用 function 來宣告函數。
 *函數的呼叫: 可以使用函數名稱來呼叫函數。

 ``` JS
function add(x, y) {
  return x + y;
}

let result = add(2, 3);
console.log(result); // 5
 ```

 ## JavaScript的基本語法：DOM操作

* DOM: Document Object Model是一個樹狀結構，代表了HTML文件的結構。
* 節點: DOM中的節點可以是元素、屬性、文字等。
* 選擇器: 選擇節點方式如下
  * document.getElementById()
  * document.getElementsByClassName()
  * document.getElementsByTagName()

``` JS
// 選擇 id 為 "myId" 的元素
let element = document.getElementById('myId');

// 選擇 class 為 "myClass" 的元素
let elements = document.getElementsByClassName('myClass');

// 選擇所有 p 元素
let paragraphs = document.getElementsByTagName('p');
```