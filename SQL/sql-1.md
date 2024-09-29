
#### 1757. Recyclable and Low Fat Products
```SQL
SELECT product_id FROM Products WHERE low_fats = 'Y' AND recyclable = 'Y';
```

#### 584. Find Customer Referee
```SQL
SELECT name FROM Customer WHERE referee_id != 2 OR referee_id IS NULL;
```

#### 595. Big Countries
```SQL 
SELECT name, population, area FROM World WHERE area >= 3000000 OR population >= 25000000;
```

#### 1148. Article Views I
```SQL
SELECT DISTINCT author_id AS id FROM Views WHERE author_id = viewer_id ORDER BY author_id ASC;
```

#### 1683. Invalid Tweets
```SQL
SELECT tweet_id FROM Tweets WHERE LENGTH(content) > 15;
```

#### 1378. Replace Employee ID With The Unique Identifier
```SQL
SELECT unique_id, name FROM Employees LEFT JOIN EmployeeUNI USING(id);
```

#### 1068. Product Sales Analysis I
```SQL
SELECT product_name, year, price FROM Product P JOIN Sales S ON P.product_id = S.product_id;
```

#### 1581. Customer Who Visited but Did Not Make Any Transactions
```SQL
SELECT customer_id, COUNT(customer_id) AS count_no_trans FROM Visits V 
LEFT JOIN Transactions T ON V.visit_id = T.visit_id WHERE T.visit_id IS NULL GROUP BY customer_id;
```

#### 197. Rising Temperature


#### 1661. Average Time of Process per Machine
```SQL
SELECT start.machine_id, ROUND(AVG(end.timestamp-start.timestamp), 3) AS processing_time
FROM Activity start JOIN Activity end ON start.machine_id = end.machine_id AND start.process_id = end.process_id AND start.activity_type = 'start' AND end.activity_type = 'end'
GROUP BY start.machine_id;
```

#### 577. Employee Bonus
```SQL
SELECT E.name, B.bonus
FROM Employee E LEFT JOIN Bonus B
ON E.empId = B.empId WHERE B.bonus < 1000 OR B.bonus IS NULL;
```
