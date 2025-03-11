# PHP

## 什麼是 PHP？

* 一種開源的程式語言：尤其適合用於 Web 開發,並且可以嵌入 HTML 中。
* Sever 端的腳本語言，也可以用於命令列 Scripting 和 desktop 應用程式開發。

## PHP 的優點包括:

* 開源且免費
* 跨平台,可以在 Windows, macOS, Linux 等多種作業系統上運行

## PHP 的缺點包括:

* 安全性問題: PHP 曾經有許多安全漏洞，特別是 SQL 注入和跨站腳本攻擊（XSS）。
* 效能問題: PHP 由於是解譯語言，缺乏即時編譯（JIT），因此可能會比其他語言（如 Java 或 C++）慢。
* 多執行緒支援有限: PHP 不支援多執行緒，對於高效能、並發應用程式來說不太適合。
* 動態型別系統: PHP 的動態型別系統可能會導致型別相關錯誤，並使程式碼更難維護。
* 語法過時: PHP 的一些語法和功能已經過時，不如其他語言的語法和功能現代。
* 函數式程式設計支援有限: PHP 不支援函數式程式設計的概念，例如閉包和高階函數。

請注意，許多這些缺點在最近的 PHP 版本中已經被解決，PHP 仍在持續演進和改進中。

## 現在常用的替代開發程式語言有:

* Python (FastAPI、Flask、Django)
* ASP.NET CORE MVC (C#)
* Ruby on Rails
* Go

## 快速建立環境

1. 安裝 Docker Desktop
2. 安裝 Docker Compose
3. Git Clone https://github.com/catseng6606/trydocker.git
4. 進入 trydocker/docker-nginx-php-mysql-phpmyadmin/ 目錄,執行 docker-compose up
5. 進入 http://localhost:7001/index.php

## PHP 基礎語法

* 變數 (Variables)
  * 變數的宣告：$ 符號的意義。
  * 變數命名規則 (例如：大小寫敏感、不能數字開頭)。
  * 變數賦值：= 運算子。
* 資料型別 (Data Types)
  * 字串 (String)：文字資料，用引號包起來 (單引號 ' 或雙引號 " 皆可)。
  * 整數 (Integer)：整數數值。
  * 浮點數 (Float)：帶有小數點的數值。
  * 布林值 (Boolean)：true 或 false。
  * 陣列 (Array)：儲存多個值的集合。
  * 物件 (Object): 略。
* 運算子 (Operators)
  * 算術運算子：+, -, *, /, % (取餘數)。
  * 賦值運算子：=, +=, -=, *=, /=。
  * 比較運算子：== (等於), != (不等於), === (嚴格等於), !== (嚴格不等於), >, <, >=, <=。
  * 邏輯運算子：&& (AND), || (OR), ! (NOT)。

## 實作：簡單的加減乘除、比較大小、邏輯判斷 

## PHP 流程控制

* 條件判斷 (Conditionals)
  * if 語句：單一條件判斷。
  * if...else 語句：二選一的條件判斷。
  * if...elseif...else 語句：多重條件判斷。
  * switch 語句：另一種多重條件判斷的方式。
* 迴圈 (Loops)
  * for 迴圈：計次迴圈。
  * while 迴圈：條件迴圈。
  * foreach 迴圈: 迴圈處理陣列

## 實作：列出 1-10 所有的單數與偶數 

