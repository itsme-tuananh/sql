UPDATE ...
SET x = x \* 10
WHERE ...;

SELECT 'hello world', 9, column / 1000 AS col ... FROM ...;

... WHERE x IS TRUE;

... WHERE date_created BETWEEN '2021-11-02' AND '2022-04-30'; (included)

... WHERE EXTRACT(DAY FROM date_fulfilled - date_created) <= 5;

SELECT _ FROM <table> LIMIT <number X>;
SELECT _ FROM <table> LIMIT <number X> OFFSET <offset number Y>;
SELECT DISTINCT \* FROM <table>;

SELECT \* FROM <table> ORDER BY <column name> ASC/DESC, <column name n> ASC/DESC, ...;

SELECT ... FROM (SELECT ... FROM ...) AS ...;
INSERT INTO ... SELECT ... FROM ...;

CREATE VIEW <view name> AS SELECT ... FROM ...;
View - Lưu trữ câu lệnh truy vấn. Câu lệnh truy vấn được gọi lại mỗi lần sử dụng View (không lưu trữ kết quả của câu lệnh truy vấn)
