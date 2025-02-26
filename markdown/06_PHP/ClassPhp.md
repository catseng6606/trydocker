# 什麼是 PHP？

PHP (Hypertext Preprocessor) 是一種開源的通用目的程式語言,尤其適合用於 Web 開發,並且可以嵌入 HTML 中。 PHP 的主要用途是用於服務端 Scripting,但是 PHP 也可以用於命令列 Scripting 和 desktop 應用程式開發。

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

