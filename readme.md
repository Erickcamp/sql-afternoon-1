# SQL afternoon project

## Table Person

- 1: create table person (
    person_id serial primary key, 
  name varchar(30),
  age integer,
  height integer,
  city varchar(50),
  favorite_color varchar(15)
    );

- 2: insert into person
    (name, favorite_color, city, height, age)
    values
    ('brynna', 'pink', 'ogden', 158, 27),
    ('blakely', 'purple', 'ogden', 106, 5),
    ('griffin', 'green', 'ogden', 95, 3),
    ('eric', 'red', 'ogden', 190, 27),
    ('kevin', 'blue', 'ogden', 190, 64);

- 3: select * from person order by height desc;

- 4: select * from person order by height asc;

- 5: select * from person order by age desc;

- 6: select * from person 
    where age > 20

- 7: select * from person 
    where age = 18

- 8: select * from person 
    where age < 20
    or age > 30

- 9: select * from person 
    where age != 27

- 10: select * from person 
    where favorite_color != 'red'

- 11: select * from person 
    where favorite_color != 'red'
    and favorite_color != 'blue' 

- 12: select * from person 
    where favorite_color = 'orange'
    or favorite_color = 'green' 

- 13: select * 
    from person
    where favorite_color in ('orange', 'green', 'blue');

- 14: select * 
    from person
    where favorite_color in ('yellow', 'purple');


## Table Orders

- 1: create table orders (
    order_id serial primary key,
  person_id integer,
  product_name varchar(30),
  product_price numeric(4, 2),
  quantity integer
    );

- 2: insert into orders
    (person_id, product_name, quantity, product_price)
    values
    (1, 'Trampoline', 1, 14),
    (2, 'Desktop', 3, 49);

- 3: select * from orders

- 4: select sum(quantity) from orders

- 5: select sum(product_price * quantity) from orders

- 6: select sum(product_price * quantity) from orders
    where person_id = 1 

## Table - artist

- 1: insert into artist 
    (name)
    values
    ('Bob Ross'),
    ('Leonardo DaVinci'),
    ('Vincent Vangough');

- 2: select * from artist order by name desc limit 10;

- 3: select * from artist order by name asc limit 5;

- 4: select * 
    from artist
    where name like ('Black%');

- 5: select * 
    from artist
    where name like ('%Black%');

## Table - employee

- 1: select first_name, last_name from employee
    where city = 'Calgary'

- 2: select birth_date from employee order by birth_date desc limit 1;

- 3: select birth_date from employee order by birth_date asc limit 1;

- 4: select * from employee 
    where reports_to = 2

- 5: select count(*) from employee
    where city = 'Lethbridge'

## Table - invoice

- 1: select count(*) from invoice
    where billing_country = 'USA'

- 2: select total from invoice order by total desc limit 1

- 3: select total from invoice order by total asc limit 1

- 4: select * from invoice
    where total > 5

- 5: select count(*) from invoice
    where total < 5

- 6: select count(*)
    from invoice
    where billing_state  in ('CA', 'TX', 'AZ')

- 7: select avg(total) from invoice

- 8 : select sum(total) from invoice
 

