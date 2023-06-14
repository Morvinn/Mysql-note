## 1.DDL

## 2.DML

## 3.DQL
### 3.5分组查询
#### 语法
```mysql
SELECT 字段列表 FROM 表名 [ WHERE 条件 ] GROUP BY 分组字段名 [ HAVING 分组 后过滤条件 ];
```
#### where与having区别
+ 执行时机不同：where是分组之前进行过滤，不满足where条件，不参与分组；而having是分组 之后对结果进行过滤。
+ 判断条件不同：where不能对聚合函数进行判断，而having可以。

### 3.6 排序查询
### 语法
```mysql
SELECT 字段列表 FROM 表名 ORDER BY 字段1 排序方式1 , 字段2 排序方式2 ;
```
+ ASC : 升序(默认值) 
+ DESC: 降序
### 3.7分页查询
### 语法
```mysql
SELECT 字段列表 FROM 表名 LIMIT 起始索引, 查询记录数 ;
```
注意：
+ 起始索引从0开始，起始索引 = （查询页码 - 1）* 每页显示记录数。 •
+ 分页查询是数据库的方言，不同的数据库有不同的实现，MySQL中是LIMIT。
+ 如果查询的是第一页数据，起始索引可以省略，直接简写为 limit 10。