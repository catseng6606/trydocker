# Table 的 CRUD
<!--TODO:請簡單說明CRUD-->
CRUD 是一種資料庫操作的基本概念，分別代表以下四種操作：

*   **C**：Create（新增），新增一筆資料到資料表中。
*   **R**：Read（讀取），讀取資料表中的資料。
*   **U**：Update（更新），更新資料表中的資料。
*   **D**：Delete（刪除），刪除資料表中的資料。
<!--TODO:請完成Mysql Table CRUD的範例-->
## MySql
### MySql 新增 Table
``` sql
CREATE TABLE users (
  id INT AUTO_INCREMENT,
  name VARCHAR(255),
  email VARCHAR(255),
  PRIMARY KEY (id)
);
```
### MySql Insert
``` sql
INSERT INTO users (name, email)
VALUES ('John Doe', 'john.doe@example.com');
```
### MySql Select
``` sql
SELECT * FROM users;
```
### MySql Update
``` sql
UPDATE users
SET name = 'Jane Doe'
WHERE id = 1;
```
### MySql Update
``` sql
DELETE FROM users
WHERE id = 1;
```

### Mysql TABLE CRUD 權限
在 MySQL 中，TABLE 的 CRUD（Create、Read、Update、Delete）相關權限可以通過 GRANT 陳述式來管理。以下是簡單的說明：

1. CREATE: 可以建立新表格
2. INSERT: 可以插入新資料到表格中
3. SELECT: 可以查詢表格中的資料
4. UPDATE: 可以更新表格中的資料
5. DELETE: 可以刪除表格中的資料

``` sql
GRANT CREATE, INSERT, SELECT, UPDATE, DELETE ON users TO 'user'@'localhost';
```

您也可以授予全部權限（包括 CREATE、INSERT、SELECT、UPDATE、DELETE 等）使用以下命令：
``` sql
GRANT ALL PRIVILEGES ON users TO 'user'@'localhost';
```

## MSSQL

### MSSQL 新增 Table
``` sql
CREATE TABLE users (
id INT IDENTITY(1,1),
name NVARCHAR(255),
email NVARCHAR(255),
PRIMARY KEY (id)
);
```

### MSSQL Insert
``` sql
INSERT INTO users (name, email)
VALUES (N'John Doe', N'john.doe@example.com');
```
### MSSQL Select
``` sql
CopyInsert
SELECT * FROM users;
```

### MSSQL Update
``` sql
UPDATE users
SET name = N'Jane Doe'
WHERE id = 1;
```

### MSSQL Delete
``` sql
DELETE FROM users
WHERE id = 1;
```

### MSQL TABLE CRUD 權限
在 Microsoft SQL Server (MSSQL) 中，TABLE 的 CRUD（Create、Read、Update、Delete）相關權限可以通過 GRANT 陳述式來管理。以下是簡單的說明：

1. CREATE TABLE: 可以建立新表格
2. INSERT: 可以插入新資料到表格中
3. SELECT: 可以查詢表格中的資料
4. UPDATE: 可以更新表格中的資料
5. DELETE: 可以刪除表格中的資料

例如，以下命令可以授予使用者 user 對 users 表格的 CRUD 權限：

``` sql
GRANT CREATE TABLE, INSERT, SELECT, UPDATE, DELETE ON users TO user;
```

您也可以授予全部權限（包括 CREATE TABLE、INSERT、SELECT、UPDATE、DELETE 等）使用以下命令：
``` sql
GRANT ALL ON users TO user;
```

或者，您可以授予更高級別的權限，例如：

1. ALTER: 可以修改表格結構
2. CONTROL: 可以控制表格的所有權限
3. REFERENCES: 可以建立外鍵

例如：
``` sql
GRANT ALTER, CONTROL, REFERENCES ON users TO user;
```

注意：在授予權限之前，請確保使用者已經存在，並且有足夠的權限。
