[TOC]

C:\Users\phuong\AppData\Local\Programs\Python\Python37\python.exe F:/programing/language/python/python-docs/readfile.py


## 1. Introduction and Overview
### 1. Download this source files first !!!!.html
### 2. Course Overview

### 3. Project Tour

![image-20200506072247776](java-e-commerce.assets/image-20200506072247776.png)  

![image-20200506072907952](java-e-commerce.assets/image-20200506072907952.png)

### 4. Project Modules

![image-20200506073119863](java-e-commerce.assets/image-20200506073119863.png)  

![image-20200506073137558](java-e-commerce.assets/image-20200506073137558.png)  

![image-20200506073157706](java-e-commerce.assets/image-20200506073157706.png)

### 5. Tools We Need

Vào marketpalce install spring tool 3

![image-20200506080446881](java-e-commerce.assets/image-20200506080446881.png)  



https://www.sequelpro.com/



## 2. Getting Started
### 1. Start Project with Index Page

https://getbootstrap.com/docs/3.4/examples/navbar/

CTRL U

download bs 3.3.7

Eclipse: file new/ Spring starter project
![image-20200506081445040](java-e-commerce.assets/image-20200506081445040.png)  

![image-20200506081814005](java-e-commerce.assets/image-20200506081814005.png)  

Check

![image-20200506081903586](java-e-commerce.assets/image-20200506081903586.png)  

Khi mới tạo file pom.xml bị lỗi

http://maven.apache.org/settings.html

https://stackoverflow.com/questions/31901320/pom-error-failure-to-find-org-springframework-boot

https://stackoverflow.com/questions/32125025/maven-and-spring-boot-non-resolvable-parent-pom-repo-spring-io-unknown-host

Obviously it's a problem with your internet connection. Check, if you can reach [http://repo.spring.io](http://repo.spring.io/) with your browser. If yes, check if you need to configure a proxy server. If no, you should contact your internet provider.

Here is the documentation, how you configure a proxy server for Maven: https://maven.apache.org/guides/mini/guide-proxies.html

old

```xml
<settings>
<proxies>
  <proxy>
    <id>proxy</id>
    <active>false</active>
    <protocol>http</protocol>
    <host>proxy.fujinet.vn</host>
    <port>8080</port>
  </proxy>
</proxies>

<mirrors>
    <mirror>
        <id>central-no-ssl</id>
        <name>Central without ssl</name>
        <url>http://repo.maven.apache.org/maven2</url>
        <mirrorOf>central</mirrorOf>
    </mirror>
  </mirrors>
  
</settings>
<!-- Author: hung-pm -->

```

new in .m2

```xml

```



### 2. Adding Carousel in Index Page
### 3. Adding More Pictures
### 4. Adding Featured-books and Non-responsive CSS
### 5. Navbar
### 6. Adding Common Part of Template
## 3. My Account
### 1. Adding MyAccount Page
### 10. Adding Create User Logic
### 11. Create New User Trouble Shooting
### 12. Wrapping MyAccount Login
### 2. Adding MyAccount Page Body
### 3. Adding User Entity, JPA, Hibernate and MySQL
### 4. Adding Security and Security Entities
### 5. Adding Security Configuration
### 6. Adding More to Login
### 7. Adding PasswordResetToken and UserService
### 8. Addin MyProfile Page
### 9. Adding New User Controller
## 4. Getting Started on Admin Portal
### 1. Entity Relationship
### 10. AdminPortal - View BookList
### 2. AdminPortal - Book Entity
### 3. AdminPortal - Home Template
### 4. AdminPortal - Login Page
### 5. AdminPortal - Add Login Function
### 6. AdminPortal - Adding New Book Form
### 7. AdminPortal - Add New Book Form - part 2
### 8. AdminPortal - Modify New Book Form
### 9. AdminPortal - Add New Book Backend Logic
## 5. BookStore Frontend
### 1. BookStore - Add Bookshelf
### 2. Bookstore - Add Book Detail Page
### 3. Bookstore - Add Book Detail Page - part 2
### 4. AdminPortal - Add BookInfo Page
### 5. AdminPortal - Add Update Book Page
### 6. AdminPortal - Add Update Book Logic
### 7. AdminPortal - Add Various Plugin
## 6. Enhance the Features
### 1. Bookstore - Adding MyProfile Controller
### 10. Bookstore - Add New Shipping Logic
### 11. Bookstore - Update Remove and SetDefault for UserShipping
### 2. Bookstore - Adding UserShipping and UserPayment
### 3. Bookstore - Add UserShipping and UserBilling Logic
### 4. Bookstore - Add CreditCard Template
### 5. Bookstore - Finish the CreditCard Page
### 6. Bookstore - Add New CreditCard Post Logic
### 7. Bookstore - Add Update CreditCard Info
### 8. Bookstore - Remove CreditCard and Set Default CreditCard
### 9. Bookstore - Add UserShiping Template
## 7. A Journey of Shopping Cart
### 1. Bookstore - Add Entities for ShoppingCart and Order
### 2. Bookstore - Add Other Entities
### 3. Bookstore - Add ShoppingCart Template
### 4. Bookstore - Add More Services and Controls
### 5. Bookstore - Add ShoppingCart Logic
### 6. Bookstore - Add Book to ShoppingCart
### 7. Bookstore - Test Adding Book to ShoppingCart
### 8. Bookstore - Update Qty and Delete function in ShoppingCart
## 8. Starting Checkout
### 1. Bookstore - Adding Checkout Page
### 2. Bookstore - Add Shipping Template
### 3. Bookstore - Add Billing Info Template
### 4. Bookstore - Add Review Items Template
### 5. Bookstore - Adding Checkout Related Services
### 6. Bookstore - Adding Checkout Info - part 2
### 7. Bookstore - Add Use This Shipping and Use This Payment
### 8. Bookstore - Add Billing the Same As Shipping
## 9. Submit Order Dance
### 1. Bookstore - Handling Order Submit
### 2. Bookstore - Add Create Order Service
### 3. Bookstore - Add Order Confirmation Email Template
### 4. Bookstore - Finish Checkout Order
### 5. Bookstore - Fix UpdateUserInfo
### 6. Bookstore - Debugging Submitting Order and Email



## 10. Some More Features

### 1. Bookstore - Add View Order Detail Template

### 2. Bookstore - Add Order Detail Controller

### 3. AdminPortal - Import Book Data

### 4. Bookstore - Scenario Testing and Bug Fixing

### 5. AdminPortal - Add Delete Book Functionality

### 6. AdminPortal - Finish Up Deleting

### 7. Bookstore - Some Other Enhancement

### 8. Bookstore - Add SearchByCategory Logic

### 9. Bookstore - Fuzzy Search

## 11. Wrap Up

### 1. Closing

======== list file ========

Process finished with exit code 0





