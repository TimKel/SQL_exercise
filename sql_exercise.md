## SQL Zoo and Codewars Practice completed;

## Products Querying
> products_db=# **INSERT INTO products (name, price, can_be_returned) VALUES ('chair', 44.00, 'false');**


> products_db=# **SELECT * FROM products;**


> products_db=# **INSERT INTO products (name, price, can_be_returned) VALUES ('stool', 25.99, 'true'),('table', 124.00, 'false');**

> products_db=# **SELECT name FROM products;**

> products_db=# **SELECT name, price FROM products;**

> products_db=# **INSERT INTO products (name, price, can_be_returned) VALUES ('tv stand', 99.95, 'false');**

> products_db=# **SELECT * FROM products WHERE price < 44.00;**
 
> products_db=# **SELECT * FROM products WHERE price BETWEEN 22.50 AND 99.99;**
 
> products_db=# **UPDATE products SET price = (price - 20);**

> products_db=# **SELECT * FROM products;**
 
> products_db=# **DELETE FROM products WHERE price < 25;**

> products_db=# **UPDATE products SET price = (price + 20);**

> products_db=# **UPDATE products SET can_be_returned = 'true';**


PLAYSTORE QUERIES

> playstore=# **SELECT * FROM analytics LIMIT 20;**
                                                    
> playstore=# **SELECT id, app_name, last_updated FROM analytics WHERE last_updated = '2018-08-01';**

> playstore=# **SELECT category, COUNT(category) FROM analytics GROUP BY category;**
  
> playstore=# **SELECT id, app_name, reviews FROM analytics ORDER BY reviews LIMIT 5;**
  
> playstore=# **SELECT id, app_name, reviews FROM analytics ORDER BY reviews desc LIMIT 5;**
 
> playstore=# **SELECT id, app_name, reviews, rating FROM analytics WHERE rating >= '4.8' ORDER BY reviews desc LIMIT 5;**
 
> playstore=# **SELECT id, app_name, reviews, rating FROM analytics WHERE rating >= '4.8' ORDER BY reviews desc LIMIT 1;**
 
> playstore=# **SELECT category, AVG(rating) as avg_rating FROM analytics GROUP BY category ORDER BY avg_rating desc;**
 
> playstore=# **SELECT app_name, price, rating FROM analytics WHERE rating < 3 ORDER BY price DESC LIMIT 1;**
 
> playstore=# **SELECT id, app_name, rating, min_installs FROM analytics WHERE min_installs < 50 AND rating > 0 ORDER BY rating DESC;**
 
> playstore=# **SELECT app_name, rating, reviews FROM analytics WHERE rating < 3 AND reviews >= 10000;**
 
> playstore=# **SELECT app_name, reviews, price FROM analytics WHERE price BETWEEN 0.10 AND 1.00 ORDER BY  reviews DESC LIMIT 10;**
  
> playstore=# **SELECT app_name, last_updated FROM analytics ORDER BY last_updated DESC;**

> playstore=# **SELECT app_name, last_updated FROM analytics ORDER BY last_updated ASC LIMIT 5;**
 
> playstore=# **SELECT app_name, last_updated FROM analytics ORDER BY last_updated ASC LIMIT 10;**
 
> playstore=# **SELECT app_name, MAX(price) FROM analytics GROUP BY app_name LIMIT 5;**
 
> playstore=# **SELECT app_name, price FROM analytics ORDER BY price DESC LIMIT 5;**
 
> playstore=# **SELECT SUM(reviews) AS all_reviews FROM analytics;**
 
> playstore=# **SELECT category FROM analytics 
playstore-#   GROUP BY category 
playstore-#   HAVING COUNT(*) > 300;**

> playstore=# **SELECT app_name, reviews, min_installs,  min_installs / reviews AS proportion
playstore-#   FROM analytics
playstore-#   WHERE min_installs >= 100000
playstore-#   ORDER BY proportion DESC
playstore-#   LIMIT 1;**
  