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
</mirrors>
  
</settings>

```

Xóa mirror thì hết lỗi

There might have been some intermittent Internet issue or something. I was facing the same problem yesterday. Updating the the project (On STS or Eclipse, right click on the project and Maven -> Update project -> tick everything except *Offline*) after sometime fixed it.

copy all file in bs3 to static folder

Create controller package, 

HomeController

```java
package com.bookstore.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {
	@RequestMapping("/")
	public String index() {
		return "index";
	}
}

```

static/style.css

```css
body {
 
}

hr {
	border: none;
	height: 1px;
	color: #333;
	background-color: #333;
}

.container {
	width: 90%;
}

.page-top {
	margin-top: -70px;
}

.navbar {
  margin-bottom: 20px;
}

.box {
	border: 1px solid red;
}

.home-headline{
	font-family: 'Times New Roman', Times, serif;
	font-size:24px;
	color: #fff;
	margin: auto;
	text-align: center;
	margin-top: -13px;
}

.home-headline span {
	background-color: #231F20;
    padding: 5px 22px;
	
}
```

template/index.html

```html

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="viewport" content="width=device-width, initial-scale=1" />

<title>Navbar Template for Bootstrap</title>

<!-- Bootstrap core CSS -->
<link href="/css/bootstrap.min.css" rel="stylesheet" />

<!-- Custom styles for this template -->
<link href="/css/style.css" rel="stylesheet" />
</head>

<body>
	<!-- Static navbar -->
	<nav class="navbar navbar-default navbar-inverse">
		<div class="container-fluid">
			<div class="navbar-header">
				<button type="button" class="navbar-toggle collapsed"
					data-toggle="collapse" data-target="#navbar" aria-expanded="false"
					aria-controls="navbar">
					<span class="sr-only">Toggle navigation</span> <span
						class="icon-bar"></span> <span class="icon-bar"></span> <span
						class="icon-bar"></span>
				</button>
				<a class="navbar-brand" href="#">Project name</a>
			</div>
			<div id="navbar" class="navbar-collapse collapse">
				<ul class="nav navbar-nav">
					<li class="active"><a href="#">Home</a></li>
					<li><a href="#">About</a></li>
					<li><a href="#">Contact</a></li>
					<li class="dropdown"><a href="#" class="dropdown-toggle"
						data-toggle="dropdown" role="button" aria-haspopup="true"
						aria-expanded="false">Dropdown <span class="caret"></span></a>
						<ul class="dropdown-menu">
							<li><a href="#">Action</a></li>
							<li><a href="#">Another action</a></li>
							<li><a href="#">Something else here</a></li>
							<li role="separator" class="divider"></li>
							<li class="dropdown-header">Nav header</li>
							<li><a href="#">Separated link</a></li>
							<li><a href="#">One more separated link</a></li>
						</ul></li>
				</ul>
				<ul class="nav navbar-nav navbar-right">
					<li class="active"><a href="./">Default <span
							class="sr-only">(current)</span></a></li>
					<li><a href="../navbar-static-top/">Static top</a></li>
					<li><a href="../navbar-fixed-top/">Fixed top</a></li>
				</ul>
			</div>
			<!--/.nav-collapse -->
		</div>
		<!--/.container-fluid -->
	</nav>

	<div class="container box">
		<div class="row">

			<!-- carousel -->
			<div class="col-xs-8">
				<div id="carousel-example-generic" class="carousel slide"
					data-ride="carousel">
					<!-- Indicators -->
					<ol class="carousel-indicators">
						<li data-target="#carousel-example-generic" data-slide-to="0"
							class="active"></li>
						<li data-target="#carousel-example-generic" data-slide-to="1"></li>
						<li data-target="#carousel-example-generic" data-slide-to="2"></li>
					</ol>

					<!-- Wrapper for slides -->
					<div class="carousel-inner" role="listbox">
						<div class="item active">
							<img src="http://lorempixel.com/output/sports-q-c-1600-500-1.jpg"
								alt="..." />
							<div class="carousel-caption">
								<h4>First Thumbnail Label</h4>
								<p>Contrary to popular belief, Lorem Ipsum is not simply
									random text. It has roots in a piece of classical Latin
									literature from 45 BC, making it over 2000 years old.</p>
							</div>
						</div>
						<div class="item">
							<img src="http://lorempixel.com/output/sports-q-c-1600-500-2.jpg"
								alt="..." />
							<div class="carousel-caption">
								<h4>First Thumbnail Label</h4>
								<p>Contrary to popular belief, Lorem Ipsum is not simply
									random text. It has roots in a piece of classical Latin
									literature from 45 BC, making it over 2000 years old.</p>
							</div>
						</div>
						<div class="item">
							<img src="http://lorempixel.com/output/sports-q-c-1600-500-3.jpg"
								alt="..." />
							<div class="carousel-caption">
								<h4>First Thumbnail Label</h4>
								<p>Contrary to popular belief, Lorem Ipsum is not simply
									random text. It has roots in a piece of classical Latin
									literature from 45 BC, making it over 2000 years old.</p>
							</div>
						</div>
						...
					</div>

					<!-- Controls -->
					<a class="left carousel-control" href="#carousel-example-generic"
						role="button" data-slide="prev"> <span
						class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
						<span class="sr-only">Previous</span>
					</a> <a class="right carousel-control" href="#carousel-example-generic"
						role="button" data-slide="next"> <span
						class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
						<span class="sr-only">Next</span>
					</a>
				</div>
			</div>
			<div class="col-xs-4"></div>
		</div>
	</div>






	<!-- Bootstrap core JavaScript
    ================================================== -->
	<!-- Placed at the end of the document so the pages load faster -->
	<script
		src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
	<script src="/js/bootstrap.min.js"></script>
</body>
</html>

```

pom.xml

```js
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<groupId>com.bookstore</groupId>
	<artifactId>bookstore</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<packaging>jar</packaging>

	<name>Bookstore</name>
	<description>frontend part for our bookstore project</description>

	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>1.4.3.RELEASE</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>

	<properties>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
		<java.version>1.8</java.version>
	</properties>

	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-thymeleaf</artifactId>
		</dependency>
	
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>


</project>

```

![image-20200506093919363](java-e-commerce.assets/image-20200506093919363.png)  

Run as/ Spring boot app

http://localhost:8080/

![image-20200506094214199](java-e-commerce.assets/image-20200506094214199.png)

### 2. Adding Carousel in Index Page



### 3. Adding More Pictures

index.html wrap carousel với panel class

```html
<body>
	<div class="page-top"
		style="width: 100%; height: 20px; background-color: #f46b42;"></div>
    
<!-- carousel -->
			<div class="col-xs-8">
				<div class="panel panel-default">
					<div class="panel-body">
                        ...
<!-- add -->
<div class="col-xs-4">
		<img src="/image/logo.png" class="img-responsive" />
</div>
                        
div class="row">
			<div class="col-xs-4">
				<div clas="panel panel-default">
					<div class="panel-body">
						<img src="/image/bestseller.png" class="img-responsive" />
					</div>
				</div>
			</div>
			<div class="col-xs-4">
				<div clas="panel panel-default">
					<div class="panel-body">
						<img src="/image/hours.png" class="img-responsive" />
					</div>
				</div>
			</div>
			<div class="col-xs-4">
				<div clas="panel panel-default">
					<div class="panel-body">
						<img src="/image/faq.png" class="img-responsive" />
					</div>
				</div>
			</div>
		</div>

		<div>
			<div class="home-headline">
				<span>Featured Books</span>
			</div>
			<hr style="margin-top: -15px;" />
		</div>


		<div class="row">
			<div id="featured-books" class="carousel slide" data-ride="carousel">
				<!-- Indicators -->
				<ol class="carousel-indicators">
					<li data-target="#featured-books" data-slide-to="0" class="active"></li>
					<li data-target="#featured-books" data-slide-to="1"></li>
					<li data-target="#featured-books" data-slide-to="2"></li>
				</ol>

				<!-- Wrapper for slides -->
				<div class="carousel-inner" role="listbox">
					<div class="item active">
						<div class="row">
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
						</div>
					</div>
					<div class="item">
						<div class="row">
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
						</div>
					</div>
					<div class="item">
						<div class="row">
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
							<div class="col-xs-2">
								<img class="img-responsive" src="/image/book1.png" />
							</div>
						</div>
					</div>
				</div>

				<!-- Controls -->
				<a class="left carousel-control" href="##featured-books"
					role="button" data-slide="prev"> <span
					class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
					<span class="sr-only">Previous</span>
				</a> <a class="right carousel-control" href="##featured-books"
					role="button" data-slide="next"> <span
					class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
					<span class="sr-only">Next</span>
				</a>
			</div>
		</div>
```

![image-20200506101140393](java-e-commerce.assets/image-20200506101140393.png)  

![image-20200506101153399](java-e-commerce.assets/image-20200506101153399.png)

### 4. Adding Featured-books and Non-responsive CSS

index.html

```css

<link href="/css/non-responsive.css" rel="stylesheet" />

<!-- Custom styles for this template -->
<link href="/css/style.css" rel="stylesheet" />

<link rel="icon" href="/image/apple-touch-icon.png" />

<body>
	<div class="page-top"

```

style.css

```css

.page-top {
	margin-top: -70px;
}
```

https://getbootstrap.com/docs/3.4/examples/non-responsive/

https://getbootstrap.com/docs/3.3/getting-started/#disable-responsive



### 5. Navbar

style.css

```css

.home-headline span {
	background-color: #231F20;
    padding: 5px 22px;
	
}
```

index.js thêm đoạn background img

```html
<!-- Wrapper for slides -->
				<div class="carousel-inner" role="listbox">
					<div class="item active">
						<img src="/image/shelf.png" class="img-responsive" />
						<div class="carousel-caption">
							<div class="row">
```

Xóa ở navbar đi

```html
<button type="button" class="navbar-toggle collapsed"
					data-toggle="collapse" data-target="#navbar" aria-expanded="false"
					aria-controls="navbar">
					<span class="sr-only">Toggle navigation</span> <span
						class="icon-bar"></span> <span class="icon-bar"></span> <span
						class="icon-bar"></span>
				</button>
```

#### Special character

& empersand

&#38

index.html

```html
<!-- Static navbar -->
		<nav class="navbar navbar-default navbar-inverse">
			<div class="container-fluid">
				<div class="navbar-header">
					<a class="navbar-brand" href="#">LE'S BOOKSTORE</a>
				</div>
				<div id="navbar">
					<ul class="nav navbar-nav navbar-left">
						<li class="dropdown"><a href="#" class="dropdown-toggle"
							data-toggle="dropdown" role="button" aria-haspopup="true"
							aria-expanded="false">BOOKS <span class="caret"></span></a>
							<ul class="dropdown-menu">
								<li><a href="#">Browse the bookshelf</a></li>
								<li><a href="#">Store hours &#38; Directions</a></li>
								<li><a href="#">FAQ</a></li>

							</ul></li>
						<form class="navbar-form">
							<div class="form-group">
								<input type="text" name="keyword" class="form-control"
									placeholder="Book title" />
							</div>
							<button type="submit" class="btn btn-default">Search</button>
						</form>
					</ul>
					<ul class="nav navbar-nav navbar-right">
						<li><a href="#">SHOPPING CART</a></li>
						<li><a href="#">MY ACCOUNT</a></li>
						<li><a href="#">LOGOUT</a></li>
					</ul>
				</div>
				<!--/.nav-collapse -->
			</div>
			<!--/.container-fluid -->
		</nav>
```



### 6. Adding Common Part of Template

common/header.html

```html
<html lang="en" xmlns:th="http://www.w3.org/1999/xhtml" >
<head th:fragment="common-header">
    
    <div th:fragment="navbar">
	<div th:fragment="body-bottom-scripts">

```

index.html

```html
<!DOCTYPE html>
<html lang="en" xmlns:th="http://www.w3.org/1000/xhtml">
<head th:replace="common/header :: common-header" />

<body>
	<div th:replace="common/header :: navbar" />
    <div th:replace="common/header :: body-bottom-scripts" />

```



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





