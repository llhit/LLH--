#### postgres数据库 ####


语句                                                                      |  作用  
----------------------------------------------------                     |---------------------
psql -U dbuser -d exampledb -h 127.0.0.1 -p 5432                         |  以新用户的名义登录数据库
sudo -u postgres psql                                                    |  登录postgres数据库
create database 数据库的名字;（默认为utf8）                                  |  创建数据库
\du                                                                      |  查看所有的用户
\l                                                                       |  查看所有的数据库
\c [database_name]例：\c test）                                           |  切换数据库
\password                                                                |  设置密码
\h                                                                       |  查看SQL命令的解释，比如\h select。
\？                                                                      |  查看psql命令列表。  
\d                                                                       |  列出当前数据库的所有表格。  
\d [table_name]                                                          |  列出某一张表格的结构。  
\e                                                                       |  打开文本编辑器。
\conninfo                                                                |  列出当前数据库和连接的信息。
TRUNCATE TABLE 表名;（例：TRUNCATE TABLE orders;）                         |  清除表中的数据（例：清除orders表中的数据）
SELECT * FROM 表名;{例：SELECT * FROM users;}                             |   查询表的内容
DELETE FROM  表名 where 条件;（例子：DELETE FROM users where id = 5;）      |  删除指定表中指定字段（例：删除users表中id=5的这条信息）
insert into 表名(字段1,字段2,字段3...) values('值1', '值2' ,'值3')           |  向表中添加内容{例：insert into users(username,password,role) values('sales','sales123','sales')}
delete from 表名 [where  条件];{例：delete from users where id=2;}         |  删除数据表中指定数据
ALTER TABLE orders DROP COLUMN shipment_number;                          |  删除表的列（语法：ALTER TABLE 表名 DROP COLUMN 要删除的列;）
ALTER TABLE orders ADD COLUMN shipment_number TEXT NOT NUll DEFAULT '';  |  添加表的列（语法：ALTER TABLE 表名 ADD COLUMN 列 （TEXT NOT NUll DEFAULT） '';）
ALTER TABLE orders ADD COLUMN should_pay_rmb DECIMAL(8,2);               |  金钱带小数（DECIMAL(8,2)） 8表示一共8个数字，小数点后面占两位
                                                                         |  
                                                                         |  
