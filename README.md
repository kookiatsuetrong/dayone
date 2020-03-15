![](ogp.png)

Day one is the first day of the rest of your life.


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

Run the web
sudo java -jar tomcat.jar --port 80 shopos.war

Setup the shop
http://xxx.xxx.xxx.xxx/setup

Finally you can login and add a category and product from the System menu.

Extracting a .war file
mkdir shopos
cd shopos
jar -xf ../shopos.war
cd ..

Don’t forget to set the outgoing email, and enable less secure email.
```

## Useful Links
```
Setup            /setup
Register         /user-register
Activation       /user-activation
Log In           /user-login
Log Out          /user-logout
Home             /user-home
Change Password  /user-change-password

Shopping Basket  /basket
View Orders      /order-list
Shipping Address /address-list

```

## Web Services


## Testing

### Compatibility Test

DBMS: MySQL, Oracle, SQL Server, DB2, PostgreSQL


### Performance Test


### Automated Test
