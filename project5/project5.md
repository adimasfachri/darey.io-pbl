# PROJECT 5: CLIENT/SERVER ARCHITECTURE USING A MYSQL RELATIONAL DATABASE MANAGEMENT SYSTEM

## CLIENT-SERVER ARCHITECTURE WITH MYSQL

### 1. First of all, Create two AWS EC2 instance, one as a MySQL server and another as MYsql Client

![create ec2 instance](https://user-images.githubusercontent.com/55023518/164701202-abb5d068-f28d-4b4c-b33d-74b4d687a397.jpg)

### 2. Install EC2 MySQL instance with ``` sudo apt install mysql-client -y ``` and ```sudo apt install mysql-client -y``` on EC2 MySQL server (don't forget to apt upgrade and apt update both instances)

### 3. On MySQL server run ```mysql_secure_installation``` for security purpose and set password for the database

### 4. After that open MySQL with sudo privilege on MySQL server and create remote user

![crea user](https://user-images.githubusercontent.com/55023518/164706927-561bc2bf-aa08-48df-8741-480fdd3a1c07.jpg)

### 5. Then, create some database and also grant that database to the remote user (in this case i create database name ```test_db```)

![create database](https://user-images.githubusercontent.com/55023518/164708247-bf714047-44d6-4b26-be06-691b20df39ac.jpg)

### 5. Don't forget to allow traffic just for the client instance on port 3306

![allow traffic](https://user-images.githubusercontent.com/55023518/164708606-53cfe8fe-a175-4623-894b-eb60e00233c6.jpg)

### 6. On the client instance, let's try to connect to the database on the server instance and show that

![done](https://user-images.githubusercontent.com/55023518/164708773-45a459b8-d9d3-474b-afbc-deed16a98250.jpg)

as you can see if we succesfully connect to the database server instace (remote_user) we can tell from the image above that we can show the database on the server instance

### 7. Finish










