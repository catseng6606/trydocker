# Table

## Mysql

<!-- TODO: 請完成針對 Mysql 的 Table 操作
    1. 使用 T-SQL 
    2. 包含新增、刪除、修改 Table （包含異動爛位與型態）的語法
-->

### Mysql 新增 Table
``` sql
CREATE TABLE users (
  id INT AUTO_INCREMENT,
  name VARCHAR(255),
  email VARCHAR(255),
  PRIMARY KEY (id)
);
```
### Mysql 刪除 Table
``` sql
DROP TABLE users;
```
### Mysql 修改 Table 名稱
``` sql
RENAME TABLE users TO new_users;
```
### Mysql 新增欄位
``` sql 
ALTER TABLE users
ADD COLUMN phone VARCHAR(20);
```
### Mysql 刪除欄位
``` sql
ALTER TABLE users
DROP COLUMN phone;
```
### Mysql 修改欄位名稱 
``` sql
ALTER TABLE users
RENAME COLUMN name TO username;
```
### Mysql 修改欄位型態
``` sql
ALTER TABLE users
MODIFY COLUMN email VARCHAR(100);
```

## MSSQL
<!-- TODO: 根據以下的架構，請完成台灣繁體中文 MSSQL 的 T-SQL 操作-->
### MSSQL 新增 Table
``` sql
CREATE TABLE users (
  id INT IDENTITY(1,1),
  name NVARCHAR(255),
  email NVARCHAR(255),
  PRIMARY KEY (id)
);
```
### MSSQL 刪除 Table
``` sql
DROP TABLE users;
```
### MSSQL 修改 Table 名稱
``` sql
EXEC sp_rename 'users', 'new_users';
```
### MSSQL 新增欄位
``` sql
ALTER TABLE users
ADD COLUMN phone NVARCHAR(20);
```
### MSSQL 刪除欄位
``` sql
ALTER TABLE users
DROP COLUMN phone;
```
### MSSQL 修改欄位名稱
``` sql
EXEC sp_rename 'users.name', 'username', 'COLUMN';
```
### MSSQL 修改欄位型態
``` sql
ALTER TABLE users
ALTER COLUMN email NVARCHAR(100);
```