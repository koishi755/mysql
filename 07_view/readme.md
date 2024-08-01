
```
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL
);
```

```
CREATE TABLE orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    order_date DATETIME NOT NULL,
    amount DECIMAL(10, 2) NOT NULL,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```


```
CREATE VIEW user_orders AS
SELECT
    users.id AS user_id,
    users.username,
    users.email,
    orders.id AS order_id,
    orders.order_date,
    orders.amount
FROM
    users
JOIN
    orders ON users.id = orders.user_id;
```


```
SELECT * FROM user_orders;
```


```
SHOW CREATE VIEW user_orders;
```
