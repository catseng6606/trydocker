# Database

## Mysql

<!-- TODO: 請完成針對 Mysql 的資料庫操作
    1. 使用 T-SQL
    2. 使用台灣繁體中文可用的語系
    3. 包含新增、刪除、修改資料庫（名稱、語系）的語法
-->

### Mysql 新增資料庫
``` sql
CREATE DATABASE mydatabase
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;
```
### Mysql 刪除資料庫
``` sql
DROP DATABASE mydatabase;
```
### Mysql 修改資料庫名稱
``` sql
RENAME DATABASE mydatabase TO newdatabase;
```
### Mysql 修改資料庫語系
``` sql
ALTER DATABASE mydatabase
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;
```
### Mysql 設定資料庫語系
``` sql
SET NAMES 'utf8mb4' COLLATE 'utf8mb4_unicode_ci';
```
<!-- DONE: 請比較以上兩者的不同-->
### Mysql 比較修改資料庫語系和設定資料庫語系的不同
#### 比較修改資料庫語系和設定資料庫語系的不同
    修改資料庫語系（ALTER DATABASE）和設定資料庫語系（SET NAMES）是兩種不同的操作，雖然它們都可以用來設定資料庫的語系，但它們的作用範圍和影響不同。

    * 修改資料庫語系（ALTER DATABASE）是用來設定整個資料庫的語系，包括所有的資料表和欄位。這個操作會影響資料庫中的所有資料，包括已經存在的資料和未來新增的資料。
    * 設定資料庫語系（SET NAMES）是用來設定連線的語系，包括連線的字符集和排序規則。這個操作只會影響當前的連線，對其他連線和資料庫中的資料不會有影響。
    
    因此，如果你想要設定整個資料庫的語系，應該使用修改資料庫語系（ALTER DATABASE）的方法。如果你想要設定連線的語系，應該使用設定資料庫語系（SET NAMES）的方法。
<!-- TODO: 根據以上的架構，請列出可以分別允許的最低權限-->
### Mysql 設定權限
1. 設定修改資料庫語系的權限
   * 需要 ALTER 權限，才能執行 ALTER DATABASE 的操作。
   * 需(要 CREATE 權限，才能建立新的資料庫。
   * 需要 DROP 權限，才能刪除資料庫。
2. 設定設定資料庫語系的權限
   * 需要 USAGE 權限，才能執行 SET NAMES 的操作。
   * 需要 EXECUTE 權限，才能執行存取資料庫的相關操作。
3. T-SQL 範例
``` sql
GRANT ALTER, CREATE, DROP ON mydatabase.* TO 'username'@'localhost';
GRANT USAGE, EXECUTE ON mydatabase.* TO 'username'@'localhost'; 
```
<!-- TODO: 根據以下的架構，請完成台灣繁體中文 MSSQL 的 T-SQL 操作-->

## MSSQL

### MSSQL 新增資料庫
``` sql
CREATE DATABASE mydatabase
COLLATE Traditional_Chinese_Taiwan_Stroke_CI_AS;
```
### MSSQL 刪除資料庫
``` sql
DROP DATABASE mydatabase;
```
### MSSQL 修改資料庫名稱
``` sql
ALTER DATABASE mydatabase
MODIFY NAME = newdatabase;
```
### MSSQL 修改資料庫語系
``` sql
ALTER DATABASE mydatabase
COLLATE = Traditional_Chinese_Taiwan_Stroke_CI_AS;
```
<!-- TODO: 根據以上的架構，請列出可以分別允許的最低權限-->
### MSSQL 設定權限
1. 設定新增資料庫的權限
    需要 CREATE DATABASE 權限，才能執行 CREATE DATABASE 的操作。
    ``` sql
    GRANT CREATE DATABASE TO [username];
    GRANT ALTER ANY DATABASE TO [username];
    ```
    需要 ALTER ANY DATABASE 權限，才能執行 ALTER DATABASE 的操作。
    ``` sql
    GRANT ALTER ANY DATABASE TO [username];
    ``` 

2. 設定刪除資料庫的權限
   需要 DROP DATABASE 權限，才能執行 DROP DATABASE 的操作。
   ``` sql
   GRANT DROP DATABASE TO [username];
   ```
3. 設定修改資料庫名稱的權限
   需要 ALTER ANY DATABASE 權限，才能執行 ALTER DATABASE 的操作。
   ``` sql
   GRANT ALTER ANY DATABASE TO [username];
   ``` 
4. 設定修改資料庫語系的權限
   需要 ALTER ANY DATABASE 權限，才能執行 ALTER DATABASE 的操作。
   ``` sql
   GRANT ALTER ANY DATABASE TO [username];
   ```
注意：[username] 需要替換成實際的使用者名稱。

另外，還可以使用以下的命令來檢視目前的權限設定：

``` sql
SELECT * FROM sys.database_permissions;
```

``` sql
SELECT * FROM sys.server_permissions;
```

## 參考網站

1. [MySQL 編碼挑選與差異比較](https://khiav223577.github.io/blog/2019/06/30/MySQL-%E7%B7%A8%E7%A2%BC%E6%8C%91%E9%81%B8%E8%88%87%E5%B7%AE%E7%95%B0%E6%AF%94%E8%BC%83/)
   * 使用 `utf8mb4_unicode_ci`：比起 `utf8mb4_general_ci` 來說，效能稍差，準確度較高。

