# SQL-ex.ru tasks
- Task #1
```sh
SELECT model, speed, hd
FROM PC
WHERE Price < 500;
```
- Task #2
```sh
SELECT DISTINCT maker
FROM Product
WHERE type = 'Printer';
```
- Task #3
```sh
SELECT model, ram, screen
FROM Laptop
WHERE price > 1000;
```
- Task #4
```sh
SELECT *
FROM Printer
WHERE color = 'y';
```
- Task #5
```sh
SELECT model, speed, hd
FROM PC
WHERE price < 600 AND cd = '12x' OR price < 600 AND cd = '24x';
```
- Task #6
```sh
SELECT DISTINCT Product.maker, Laptop.speed
FROM Laptop
JOIN Product
ON Product.model = Laptop.model
WHERE Laptop.hd >= 10;
```
- Task #7
```sh
SELECT model, price 
FROM PC 
WHERE model IN (SELECT model 
 FROM Product 
 WHERE maker = 'B' AND 
 type = 'PC')
UNION
SELECT model, price 
FROM Laptop 
WHERE model IN (SELECT model 
 FROM Product 
 WHERE maker = 'B' AND 
 type = 'Laptop')
UNION
SELECT model, price 
FROM Printer 
WHERE model IN (SELECT model 
 FROM Product 
 WHERE maker = 'B' AND 
 type = 'Printer');
```
- Task #8
```sh
SELECT DISTINCT maker
FROM Product
WHERE type in ('PC')
EXCEPT
SELECT DISTINCT maker
FROM Product
WHERE type in ('Laptop');
