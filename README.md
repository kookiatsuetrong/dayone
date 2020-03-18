![](ogp.png)


## Demo
The demo web site: http://codestar.work:3000

## Installation

```
From Ubuntu:

Update repository:
sudo apt update

sudo apt install mysql-server
sudo mysql --execute="create database shopos default charset 'UTF8';"
sudo mysql --execute="create user james identified with mysql_native_password by 'bond';"
sudo mysql --execute="grant all on shopos.* to james;"

Install OpenJDK:
sudo apt install default-jdk

Download Tomcat or Jetty stand-alone edition
wget https://codestar.work/tomcat.jar
wget https://codestar.work/jetty.jar

Download Shop OS
wget https://codestar.work/shopos.war

Extracting a .war file
mkdir shopos
cd shopos
jar -xf ../shopos.war
cd ..

sudo java -jar tomcat.jar --port 80 shopos

Setup the shop
http://xxx.xxx.xxx.xxx/setup

Finally you can login and add a category and product from the System menu.
Don’t forget to set the outgoing email, and enable less secure email.

```

## Useful Links
```
Setup              /setup
Register           /user-register
Activation         /user-activation
Log In             /user-login
Log Out            /user-logout
Home               /user-home
Change Password    /user-change-password

Shopping Basket    /basket
View Orders        /order-list
Shipping Address   /address-list
```

## Web Services

Check Service
```
curl                http://localhost:3000/service/check
curl --request POST http://localhost:3000/service/check-post
```

Log In with Email and Password
```
curl \
--data 'email=user@email.com&password=password' \
--verbose \
--request POST http://localhost:3000/service/user-login
```

Check status of current user
```
curl http://localhost:3000/service/user-current
curl \
--header 'Cookie: JSESSIONID=WXYZ;' \
http://localhost:3000/service/user-current
```

## Application Servers

### Tomcat


### Jetty


### GlassFish

### Open Liberty
```
bin/server create dayone
cp dayone.war usr/servers/dayone/apps

vi usr/servers/dayone/server.xml

<?xml version="1.0" encoding="UTF-8"?>
<server description="new server">
    <featureManager>
        <feature>servlet-4.0</feature>
    </featureManager>

    <httpEndpoint id="app" host="*" httpPort="9001" />
    <webApplication contextRoot="/" location="dayone.war" />
    <applicationManager autoExpand="true"/>
</server>
```

## Database Management System

### MySQL
```
sudo apt install mysql-server
sudo mysql --execute="create database shopos default charset 'UTF8';"
sudo mysql --execute="create user james identified with mysql_native_password by 'bond';"
sudo mysql --execute="grant all on shopos.* to james;"
```

### PostgreSQL
```
sudo apt update
sudo apt install postgresql
sudo --user postgres psql
\password
\q
sudo --user postgres createdb shopos
sudo --user postgres psql -d shopos
```

And change the persistence.xml as follow:
```
Driver:     org.postgresql.jdbc.Driver
URL:        jdbc:postgresql://localhost/shopos
User:       postgres
Password:   xxxx
```

### Derby


## Docker
How to use it with Docker.

## Testing

### User Acceptance Test (UAT)

General System:

User Registration:

Password Recover:

User Settings:

Checkout and Address:

User Management:

Product and Category Management:



### Compatibility Test

DBMS: MySQL, Oracle, SQL Server, DB2, PostgreSQL


### Performance Test


### Automated Test
The Selenium project is here: https://github.com/kookiatsuetrong/dayone-selenium


## React Native
The React Native mobile application is here: https://github.com/kookiatsuetrong/dayone-mobile

## Theme Customization
```
+ dayone
  +-- images
  +-- public
      +-- css
      +-- js
  +-- theme
      +-- xxxx.html
      +-- xxxx.html
      +-- xxxx.html
  +-- WEB-INF
      +-- web.xml
      +-- web-servlet.xml
```   
      
## Ticket System
The technical support ticket system is here: https://github.com/kookiatsuetrong/dayone-support


