# PROJECT 4: MEAN STACK IMPLEMENTATION

## Implement a simple Book Register web form using MEAN stack

### 1. first of all update, upgrade and add certificates on ubuntu 
#### ```sudo apt update -y && sudo apt upgrade -y && sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates && curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - ```

### 2. Install node.js and mongoDB with
#### ```sudo apt-get install -y nodejs && sudo apt install -y mongodb ```

![nodejs and mongodb install](https://user-images.githubusercontent.com/55023518/163662833-8d685bdf-12f6-455d-9833-6dbd8f46ddc4.jpg)


### 3. install body-parser package with 
#### ```sudo npm install body-parser```

### 4. run  ```npm init ``` and create server.js file

![cat server js](https://user-images.githubusercontent.com/55023518/163662854-3d52aa3c-1023-4b03-ab9c-ddb1a5f42794.jpg)

### 5. Install Express and set up routes to the server
#### ```sudo npm install express mongoose```

### 6. create apps dir than make routes.js, Create models dir than make book.js, create public dir than make script.js and index.html (fill a code from the requirement on each file)

![creat code file](https://user-images.githubusercontent.com/55023518/163663107-e4738a30-05e3-4146-8b38-7df016d36c45.jpg)

### 7. Finally run the web app with ```node server.js``` don't forget to open port 3000 on aws instance

![final node](https://user-images.githubusercontent.com/55023518/163663822-15304b2b-cca1-44b0-b056-02840611e750.jpg)






