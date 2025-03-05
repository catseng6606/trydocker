# 基本的條件查詢

基本的條件查詢（WHERE 子句）有以下常用的項目：

## 等值查詢使用 = 符號進行等值查詢。
``` sql
SELECT * FROM table_name WHERE column_name = 'value';
```
## 不等值查詢使用 <> 或 != 符號進行不等值查詢。
``` sql
SELECT * FROM table_name WHERE column_name <> 'value';
SELECT * FROM table_name WHERE column_name != 'value';
```

## 大於查詢使用 > 符號進行大於查詢。
``` sql
SELECT * FROM table_name WHERE column_name > 'value';
```

## 小於查詢使用 < 符號進行小於查詢。

``` sql
SELECT * FROM table_name WHERE column_name < 'value';
```

## 大於等於查詢使用 >= 符號進行大於等於查詢。

``` sql
SELECT * FROM table_name WHERE column_name >= 'value';
```

## 小於等於查詢使用 <= 符號進行小於等於查詢。

``` sql
SELECT * FROM table_name WHERE column_name <= 'value';
```

## LIKE 搜尋使用 LIKE 符號進行模糊搜尋。

``` sql
SELECT * FROM table_name WHERE column_name LIKE '%value%';
```
## IN 搜尋使用 IN 符號進行多值搜尋。

``` sql
SELECT * FROM table_name WHERE column_name IN ('value1', 'value2', 'value3');
```

## NOT IN 搜尋使用 NOT IN 符號進行多值排除搜尋。

``` sql
SELECT * FROM table_name WHERE column_name NOT IN ('value1', 'value2', 'value3');
```

## IS NULL 搜尋使用 IS NULL 符號進行空值搜尋。

``` sql
SELECT * FROM table_name WHERE column_name IS NULL;
```
## IS NOT NULL 搜尋使用 IS NOT NULL 符號進行非空值搜尋。

``` sql
SELECT * FROM table_name WHERE column_name IS NOT NULL;
```

## ETWEEN 搜尋使用 BETWEEN 符號進行範圍搜尋。

``` sql
SELECT * FROM table_name WHERE column_name BETWEEN 'value1' AND 'value2';
```

## NOT BETWEEN 搜尋使用 NOT BETWEEN 符號進行範圍排除搜尋。

``` sql
SELECT * FROM table_name WHERE column_name NOT BETWEEN 'value1' AND 'value2';
```

這些是基本的條件查詢項目，可以用來構造更複雜的查詢條件。

## 實作：如何透過 AI 增加查詢效能