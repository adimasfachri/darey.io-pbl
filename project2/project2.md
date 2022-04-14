# PROJECT 1: LEMP STACK IMPLEMENTATION

## 1. Install nginx and verify with ```sudo apt install -y nginx && sudo systemctl status nginx```

![install nginx](https://user-images.githubusercontent.com/55023518/163154026-9feb5dc4-6bc1-4416-8642-9043cac4f86c.jpg)
![install nginx](https://user-images.githubusercontent.com/55023518/163154339-a0888183-f8b8-4c60-a3cc-d12cec996e67.jpg)

## 2. Open port 80 on aws instance that run nginx and verify that my nginx run properly

![welcome to nginx](https://user-images.githubusercontent.com/55023518/163156673-d4685cd6-6144-4ee7-859a-f33d3ec29b26.jpg)

## 3. Install mySQL database with ```sudo apt install mysql-server -y``` and verify if we able to log in to the MySQL console with ```sudo mysql```

![mysql](https://user-images.githubusercontent.com/55023518/163167041-86b17032-496a-4781-8fdd-9412240d6492.jpg)

## 4. Install PHP with ```sudo apt install -y php-fpm php-mysql```
## 5. Configuring Nginx to Use PHP Processor and create new domain

![config nginx](https://user-images.githubusercontent.com/55023518/163469702-9e58a615-e51a-453d-bdc8-ef67e05d460a.jpg)

## 4. dont forget to tell Nginx to use the configuration next time it is reloaded with ```sudo nginx -t```

## 5. verify nginx can serve out sample html 

![verify nginx](https://user-images.githubusercontent.com/55023518/163476225-ca2f1a6d-5bd5-4a37-9c68-6af461948c97.jpg)

## 6. Testing PHP with Nginx, verify Nginx can correctly hand .php files off to your PHP processor

![verify php](https://user-images.githubusercontent.com/55023518/163477056-a999782e-724f-43e5-a24b-f75bb4e2e583.jpg)
![verify php2](https://user-images.githubusercontent.com/55023518/163477339-0b8c7b0a-8b4d-456d-9974-4befdaa52cb3.jpg)

## 7.  Retrieving data from MySQL database with PHP. Creates a new user named example_user, using mysql_native_password as default authentication method and   create a test table named todo_list

![mysql table](https://user-images.githubusercontent.com/55023518/163480189-d2252b5f-4b3f-493c-ba88-72470c7683f5.jpg)

## 8. Create ```todo_list.php script``` and output the database to nginx with php 
![todo php](https://user-images.githubusercontent.com/55023518/163480593-240e1bb6-1fb7-4505-976d-fbc9ade1b777.jpg)





