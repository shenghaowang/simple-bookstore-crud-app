# Simple Bookstore CRUD App

A mini golang project for demonstrating the CRUD operations of a book management system.

## MySQL Setup for Linux
1. Install MYSQL locally with the following commands.
```
sudo apt update
sudo apt install mysql-server
sudo mysql_secure_installation
sudo mysql
mysql -u root -p
mysql -u sammy -p
systemctl status mysql.service
sudo mysqladmin -p -u sammy version
```

2. Start mysql by running `sudo mysql`.

3. Create a database for this project, which can be named as "sandbox".
```
create database sandbox;
```

4. Create a user for using MySQL.
```
CREATE USER 'mysqluser'@'localhost' IDENTIFIED BY 'mysqlpwd';
```

5. Grant privileges to the user.
```
GRANT ALL PRIVILEGES ON * . * TO 'mysqluser'@'localhost';
FLUSH PRIVILEGES;
```

6. Verify the existence of the created user.
```
select Host, User from mysql.user;
```

7. Exit mysql.

8. To fix the MySQL error: "Resolving the 'Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock' (2)' Error"
https://phoenixnap.com/kb/mysql-server-through-socket-var-run-mysqld-mysqld-sock-2

- Check the status of the MySQL service with `sudo systemctl status mysql`
- If the service is not running, restart with `sudo systemctl start mysql`

## References
* [How to Use MySQL Database in Go with GORM: A Step-by-Step Guide](https://www.sqliz.com/posts/golang-gorm-mysql/)