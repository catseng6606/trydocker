# 資料庫基礎
## 什麼是資料庫？

## 資料庫基本概念

1. **資料庫的定義**：資料庫是一種用於儲存和管理資料的軟體系統。
2. **常見的資料庫類型**：關聯式資料庫、NoSQL資料庫、雲端資料庫等。
3. **使用者、資料表、欄位、資料**：資料表是資料庫中用於存儲數據的基本單元，欄位是資料表中用於存儲特定數據的欄位，資料是存儲在資料表中的具體數據。
4. **資料庫的用途**：資料庫用於存儲和管理數據，提供數據的查詢、更新、刪除等功能。

## SQL 基礎語法

1. SQL 是什麼？：SQL（Structured Query Language）是一種用於管理關聯式資料庫的語言。
2. Create Table：建立資料表的語法，例如 `CREATE TABLE users (id INT, name VARCHAR(255), email VARCHAR(255));`
3. INSERT INTO：新增資料到資料表的語法，例如 `INSERT INTO users (id, name, email) VALUES (1, 'John Doe', 'john@example.com');`
4. SELECT：查詢資料表的語法，例如 `SELECT * FROM users WHERE id = 1;`
5. WHERE：篩選資料的語法，例如 `SELECT * FROM users WHERE name = 'John Doe';`
6. UPDATE：更新資料表的語法，例如 `UPDATE users SET name = 'Jane Doe' WHERE id = 1;`
7. DELETE：刪除資料表的語法，例如 `DELETE FROM users WHERE id = 1;`
8. JOIN：結合多個資料表的語法，例如 `SELECT * FROM users INNER JOIN orders ON users.id = orders.user_id;`

## 基本的資料庫管理

1. **資料庫備份**：定期備份資料庫以防止資料丟失。
    * MsSql：使用 SSMS 的備份功能，可搭配維護計畫執行排程任務。
    * MySql：使用 mysqldump 工具與搭配排程任務，`crontab`。
    * 備份類型：完整備份、差異備份、交易記錄備份
    * 備份頻率：每日、每週、每月
    * 備份保存期限：30 天、60 天、90 天

2. **資料庫更新**：定期更新資料庫軟體以確保安全性和效能。
    * 軟體更新，資料庫引擎、驅動程式、工具
    * 結構更新：資料庫結構、索引、View 的更新與維護工作

3. **資料庫優化**：定期優化資料庫結構和查詢以提高效能。
    * 結構優化：索引、View、觸發程式
    * 查詢優化：SQL 語法、查詢計畫、索引使用

4. **資料庫安全**：設定適當的權限和安全措施以防止未經授權的存取。
    * 權限設定：使用者角色、資料庫權限、表格權限
    * 安全措施：密碼設定、連線加密、防火牆設定

5. **資料庫監控**：定期監控資料庫的效能和安全性以快速發現問題。
    * 效能監控：CPU 使用率、記憶體使用率、磁碟使用率
    * 安全性監控：登入嘗試、資料庫錯誤、安全性警告

6. **資料庫備份恢復**：建立備份恢復程序以確保資料庫在發生問題時可以快速恢復。
    * 備份恢復程序：手動恢復、自動恢復
    * 恢復測試：定期測試備份恢復程序

7. **資料庫資料清理**：定期清理資料庫中的垃圾資料以保持資料庫的健康。
    * 資料清理：刪除無用資料、更新資料、合併資料

8. **資料庫索引管理**：定期管理資料庫中的索引以提高查詢效能。
    * 索引建立：建立新索引、更新索引
    * 索引維護：重建索引、更新統計資料

9. **資料庫查詢優化**：定期優化資料庫中的查詢以提高效能。
    * 查詢分析：分析查詢計畫、查詢執行時間
    * 查詢優化：優化 SQL 語法、優化索引使用

10. **資料庫版本控制**：使用版本控制系統來管理資料庫的變更和更新。
    * 版本控制系統：Git、SVN、TFS
    * 資料庫版本控制：管理資料庫結構變更、管理資料庫資料變更

## 實作：基礎 SQL 操作