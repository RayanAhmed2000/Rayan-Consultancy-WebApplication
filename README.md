# Rayan-Consultancy-WebApplication
## Creating database server
```
sudo apt-get update
sudo apt-get install mysql-server -y
sudo mysql_secure_installation
sudo systemctl start mysql
sudo systemctl enable mysql
```
- login into database
```
sudo mysql -u root -p
exit;
```
- make database remotely accessible
```
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```
- change the binding address to 0.0.0.0
```
sudo systemctl restart mysql
```
- create a user and login
```
sudo mysql -u root -p
CREATE USER 'rayan'@'%' IDENTIFIED BY 'Admin@123';
GRANT ALL PRIVILEGES ON *.* TO 'rayan'@'%';
FLUSH PRIVILEGES;
```
- exit database and allow port 3306
```
sudo ufw allow 3306
```

## Creating database client server 
### Same installation steps
### To connect to database enter commnd
```
mysql -u rayan -h <PublicIP> -p
```

