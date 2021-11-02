# SQL-ex.ru tasks
- Task #1
```sh
select model, speed, 
hd from PC 
where price <500;
```
- Task #2
```sh
select distinct maker
from Product 
where type = 'Printer';
```
- Task #3
```sh
select model, ram, screen 
From Laptop 
where price > 1000;
```
- Task #4
```sh
select * 
from Printer 
where color = 'y';
```
- Task #5
```sh
select model, speed, hd 
from PC 
where (cd = '12x' or cd = '24x') and price < 600;
```
- Task #6
```sh
select distinct product.maker, laptop.speed
from product 
join laptop on product.model = laptop.model
where hd >= 10
order by speed;
```
- Task #7
```sh
select a.model, price 
from (select model, price 
from PC 
union
select model, price 
from Laptop
union
select model, price 
from Printer) 
as a join
Product p on a.model = p.model
where p.maker = 'B';
```
- Task #8
```sh
select distinct maker
from Product
where type in ('PC')
except
Select distinct maker
from Product
where type in ('Laptop');
```
- Task #9
```sh
select distinct maker 
from Product
join PC on pc.model = product.model
where speed >= 450;
```
- Task #10
```sh
select model, price
from Printer
where price = (select max(price) from Printer);
```
- Task #11
```sh
select avg(speed) as avg_speed
from PC;
```
- Task #12
```sh
select avg(speed) as avg_speed
from Laptop
where price > 1000;
```
- Task #13
```sh
select avg(speed) as avg_speed
from PC
join Product on product.model = pc.model
where product.maker = 'A';
```
- Task #14
```sh
select classes.class, ships.name, classes.country
from Ships
join Classes on classes.class = ships.class
where numGuns >= 10;
```
- Task #15
```sh
select hd
from PC 
group by hd
having count(model) > 1;


