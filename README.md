## Homework : 1

### Film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.
~~~sql 
SELECT title , description FROM film;
~~~

### Film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
~~~sql  
SELECT * FROM film WHERE length >= 60 and length <= 75 ;
~~~

### Film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
~~~sql 
SELECT * FROM film WHERE rental_rate = 0.99 and replacement_cost = 12.99 or rental_rate = 0.99 and replacement_cost = 28.99 ; 
~~~

### Customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
~~~sql 
SELECT last_name FROM customer WHERE first_name = 'Mary';
~~~

~~~sql  
SELECT * FROM film WHERE length < 50 and NOT rental_rate = 2.99 or length < 50 and NOT rental_rate = 4.99;
~~~

## Homework : 2

~~~sql
SELECT * FROM film WHERE replacement_cost BETWEEN 12.99 and 16.99;
~~~

~~~sql
SELECT first_name , last_name FROM actor WHERE first_name  IN ('Penelope', 'Nick', 'Ed');
~~~

~~~sql 
SELECT * FROM film WHERE rental_rate  IN (0.99, 2.99, 4.99) and replacement_cost IN (12.99, 15.99, 28.99);
~~~

## Homework : 3

~~~sql 
SELECT country FROM country WHERE country ~~ 'A%a' ;
~~~

~~~sql 
SELECT country From Country WHERE LENGTH(country) >= 6 AND country ~~'%n';
~~~

~~~sql 
SELECT title FROM film WHERE title ~~* '%t%t%t%t%';
~~~

~~~sql 
SELECT * FROM film WHERE title ~~ 'C%' and length > 90 and rental_rate = 2.99 ;
~~~








