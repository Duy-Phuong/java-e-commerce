[TOC]



---



C:\Users\phuong\AppData\Local\Programs\Python\Python37\python.exe F:/programing/language/python/python-docs/readfile.py
======== name dir ========
## 1. Introduction
### 1. Introduction



### 2. IMPORTANT BROWSERS FOR THIS COURSE.html

#### `**IF YOU ARE JUST STARTING OUT, PLEASE READ THE WHOLE ARTICLE**`



```
UPDATE:
```

***THESE ISSUES HAVE BEEN RESOLVED***

Please wait until you get to those sections of the course so it is not out of context, you need chrome with extensions for the development phase anyway:



FIX #1: https://www.udemy.com/full-stack-project-spring-boot-20-react-redux/learn/v4/t/lecture/12143810?start=75

FIX #2: https://www.udemy.com/full-stack-project-spring-boot-20-react-redux/learn/v4/t/lecture/12201742?start=0

```
INITIAL PROBLEM:
```

**Please note that this app works fine on: Firefox, Safari and Chrome. If you are on Chrome and it loads blank, then please install react dev tools and redux dev tools on Chrome. You need Chrome and these dev tools to follow the course.**

https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en

https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en

**Please also note that this is a known issue in the React/Redux community:** https://github.com/reduxjs/redux/issues/2359

**I'll be investigating how to configure the store for Internet Explorer and Edge, but for now in order to check the prototype in Heroku (**https://agileintppmtool.herokuapp.com/) **please use Chrome (with extensions) or Firefox (MacOS and Windows) or Safari (MacOS)**

### 3. WATCH BEFORE YOU BUY App Demo (Prototype)



### 3.1 httpsagileintppmtool.herokuapp.com.html



### 4. WATCH BEFORE YOU BUY Requirements, IDEs, Support

https://agileintppmtool.herokuapp.com/

![image-20200507114829589](spring-boot-20-react-redux.assets/image-20200507114829589.png)

123456

![image-20200507114859098](spring-boot-20-react-redux.assets/image-20200507114859098.png)  

![image-20200507115035457](spring-boot-20-react-redux.assets/image-20200507115035457.png)

![image-20200507115050182](spring-boot-20-react-redux.assets/image-20200507115050182.png)

![image-20200507115252651](spring-boot-20-react-redux.assets/image-20200507115252651.png)  

![image-20200507115322458](spring-boot-20-react-redux.assets/image-20200507115322458.png)  



### 5. REVIEW BEFORE YOU START- Mindset and Course's scope.html

Please have the right mindset for this course and for any other software development course that you are taking or planning to take.

> #### **Here is a torpedo of truth:**

#### **No** six-figure worth, debt-binding university degree, **no** hefty 5-figure worth coding bootcamp, **no** course or book **covers it all**. **No one does**, **no one can!**



The times I have seen people trying to cover it all then one of two things happen:

· A good chunk of those topics are covered in a very contrive and virtually useless way just to say “I covered it all”

· And THE VERY FEW who did covered it all ended up releasing an ENDLESS course or book THAT NO ONE FINISHES ANYWAY!

No project that I have ever worked on has ever used all of JAVA or all of any tech stack involved. In some projects you use some features, in some you use others. **This course is a project so we will only use and explain the features of the TECH STACK that we need to use in order for us to implement and \*manually\* test the functionality that is in scope.**

**With that in mind, when you join this course you do so completely aware that anything that is not explicitly covered in this course is out of scope, no exceptions.** If you have recommendations, please let me know. Depending on the topic I might include it in upcoming courses or create a course on the matter.

Software development courses should be seen as a “**gateway**” for you to grab new skills and also to have a better understanding of how far you want to go. No educational material should ever be seen as “All that you need for a brilliant Software Developer career”. They are all stepping stones for you to build your skills and compete in the job market.

**Please have the right expectations at all times.**

## 2. Spring Backend - Basic CRUD Operations - Project
### 1. IMPORTANT PLEASE USE JAVA 8.html

Hi Team: `***\**No TLDR!!! This is important, make sure you scroll all the way down\**\***`

In the next video you will notice that I set my project to work with Java 8. Please make sure that you are using Java 8 in you environment for this project.

**How can I check this?**

In your terminal please run the following command: java -version

If you see anything that is **not** Java 8, then you need to set your env to this version.

In case you need to have several versions of Java in you env, a good option, that I personally use, is sdkman.io, this allows you to install the versions of Java that you need and jump from one to the other when needed. again: sdkman.io. You need to read the documentation and install it properly, **please note that supporting this is not in the scope of this course**. Follow the instructions and you should be fine.

***Why is that, I mean Java 9 and Java 10 are out? Why not use the latest?\***

First let me say this, Java 8 is an LTS (Long term support) version of Java, while Java 9 and 10 are actually non-LTS, moreover Oracle is not even supporting them anymore. Java 9 was supported until March 2018 and 10 was supported until September 2018, see for yourselves: https://www.oracle.com/technetwork/java/javase/eol-135779.html.

It is a common recommendation to always stick to LTS versions of the stack you are using. With java 9 there is a lot that breaks (google it, many complains about this particular version) and too many work arounds required. We are not doing anything that requires features in Java 9 or 10 so please refrain from using those versions for this project.

Please stick with Java 8 for now. Once the landscape is clearer around Java11 (Released on September 2018) then I will be sure to update you all accordingly.

**Issues running spring-boot 2.0 on Java 9:** https://github.com/**spring-projects**/**spring-boot**/issues/12462

### 
### 2. Folder Structure and Github setup

https://start.spring.io/

hoặc có thể dùng intelliji

Adding screenshot from latest 2019.2 IDEA Ultimate Edition:

- Go to `File -> Settings -> Plugins`
- search for `spring boot` under `Installed` plugins list
- Press the `Enable` button
- Restart IDE

https://stackoverflow.com/questions/32476228/intellij-spring-initializr-not-available

![image-20200507144331578](spring-boot-20-react-redux.assets/image-20200507144331578.png)

![image-20200507144823022](spring-boot-20-react-redux.assets/image-20200507144823022.png)  

![image-20200507145030712](spring-boot-20-react-redux.assets/image-20200507145030712.png)  

Chọn location D:\Source\spring boot\ppmtool

```shell
git branch
git branch branch0
git checkout branch0
git push --set-upstream origin branch0
git merge branch0 # merge to master
git push

```





### 2.1 branch0.html

https://github.com/AgileIntelligence/AgileIntPPMTool/tree/branch0

### 2.2 Initial Repository.html

https://github.com/AgileIntelligence/ppmtool

### 2.3 Git Branch Tutorial.html

https://www.atlassian.com/git/tutorials/using-branches

### 3. IMPORTANT - READ THROUGH About H2 Database.html

**Please read through.**

In the next video, we are going to create our object and test whether or not the table gets created in the H2 database. I have received an unexpected number of reports that after opening the H2 database console, the table is not present.

**I want to clarify the following pointers:**

1. I want to remind you, that **previous basic experience with the Spring Framework is expected for this course**. This was clearly discussed in the **"WATCH BEFORE YOU BUY: Requirements, IDEs, Support"** video **(Do not skip this video)**

   https://www.udemy.com/full-stack-project-spring-boot-20-react-redux/learn/v4/t/lecture/11792132/?instructorPreviewMode=student_v4

2. You need to make sure that you have **the correct folder structure for your Spring Boot project**

3. Check the **Q&A in this lecture**, read through, and **try a different JDBC URL** if the one out of the box doesn't work for you

4. Make sure that you have the right **@Entity import (Please, check your code against mine)**

5. Finally, since you have previous experience, **do not get hung up on the H2 database not working** (which should not be the case) **just set up MySQL or any other DB that you are already comfortable with**. Later in the course we will set up MySQL anyway.

Thank you for your attention.

### 4. Project Object & Project Repository- branch1
### 4.1 branch1.html



### 5. Project Service & Project Controller  Create first project - branch2
### 5.1 branch2.html
### 6. Set up project object validation - branch3
### 6.1 branch3.html
### 7. Project Object Validation part1 - branch4
### 7.1 branch4.html
### 8. Project Object Validation part2 - branch5
### 8.1 branch5.html
### 9. Refactor Project Controller -branch6
### 9.1 branch6.html

### 10. Custom Exceptions for Unique Project Identifiers - branch7

### 10.1 branch7.html

### 11. Find Project by Identifier - branch8

### 11.1 branch8.html

### 12. Find All Projects - branch9

### 12.1 branch9.html

### 13. Delete an existing project - branch10

### 13.1 branch10.html

### 14. Update an existing project

## 3. React & Redux Front-end Project CRUD Operations
### 1. Introduction to React and Redux
### 10. IMPORTANT React + Redux Architecture and Support
### 11. Create Redux Store - branch18
### 11.1 branch18.html
### 12. Create Project from React - branch19
### 12.1 branch19.html
### 13. Get validation errors from Redux - branch20
### 13.1 branch20.html
### 14. Style validation errors with classnames - branch21
### 14.1 branch21.html
### 15. Get Projects - redux only - branch22
### 15.1 branch22 - made offline changes, check both commit 3e53bc8  and 1 parent 71370a3.html
### 16. Get Projects - final step - branch23
### 16.1 branch23.html
### 17. Update Project use case architecture
### 18. Update Project form and route
### 18.1 branch24.html
### 19. Get Project by Id, Update use case part 1 - commit id b13741f
### 19.1 commit.html
### 2. Set up development Environment for React Development
### 20. Persist Project Object Updates - branch26
### 20.1 branch26.html
### 20.2 branch26.html
### 21. Handle Errors in UpdateProject.js  - branch27
### 21.1 branch27.html
### 22. BUG FIX Strange Update Behaviour
### 22.1 branch28.html
### 23. Delete Project Architecture
### 24. Delete an existing project - branch29
### 24.1 branch29.html
### 25. Refactor Delete Operation and Proxy
### 25.1 branch30.html
### 3. Create and review Boiler Plate react app - branch11
### 3.1 branch11.html
### 4. first react component - branch12
### 4.1 branch12.html
### 5. Project and header components - branch13
### 5.1 branch13.html
### 6. Bringing Bootstrap 4+ - branch14
### 6.1 branch14.html
### 7. Style our Dashboard, Navbar, ProjectItem - branch15
### 7.1 branch15.html
### 8. React Router, first Functional component - branch16
### 8.1 branch16.html
### 9. AddProject Component - controlled form - branch 17
### 9.1 ReactJS documentation on controlled forms.html
### 9.2 branch17.html
## 4. Add Project Tasks - Backend
### 1. Backlog and ProjectTask Entities - branch31
### 1.1 branch31.html
### 10. Find ProjectTask by projectSequence (happy path)-branch38
### 10.1 branch38.html
### 11. Find ProjectTask by projectSequence wValidation - branch39
### 11.1 branch39.html
### 12. Update project task (happy path)-branch40
### 12.1 branch40.html
### 13. Finish up with update validation and delete - branch41
### 13.1 branch41.html
### 14. BUG FIX delete operation, improved backlogproject task rel - branch42
### 14.1 branch42.html
### 2. Entity Relationships Project and Backlog - branch32
### 2.1 branch32.html
### 3. Backlog - ProjectTask relationship - branch33
### 3.1 branch33.html
### 4. Design discussion around creating a Project Task
### 5. Persist Project Task (Bug fix pending setPriority) - branch34
### 5.1 branch34.html
### 6. BUG FIX ProjectTask priority, projectIdentifier, PTSequence - branch35
### 6.1 branch35.html
### 7. Get Project Backlog (happy path) - branch36
### 7.1 branch36.html
### 8. SET UP THE PROJECT TO USE MYSQL, NO MORE H2!
### 9. Handle Project Not Found Exception  Project Tasks-branch37
### 9.1 branch37.html
## 5. Add Project Tasks - React  Redux
### 1. Intro to Section, Demo of what we are implementing
### 1.1 checkout the prototype in this demo.html
### 10. Load ProjectTasks to the state - branch50
### 10.1 branch50.html
### 11. Load Project Tasks to UI step 1 - branch51
### 11.1 branch51.html
### 12. Organize Project Tasks by status and priority - branch52
### 12.1 branch52.html
### 13. ProjectBoard Algorithm - branch53
### 13.1 branch53.html
### 14. update Project task part 1 - branch54
### 14.1 branch54.html
### 15. Update Project task part 2 - branch55
### 15.1 branch55.html
### 16. Update Project task part 3- branch56
### 16.1 branch56.html
### 17. Delete Project Task - branch57
### 17.1 branch57.html
### 2. BUG FIX Import error in Backlog reducer - branch43.html
### 3. Types and Reducers for Project Tasks - branch43
### 3.1 branch43.html
### 4. Section designs and Folder Structure - branch44
### 4.1 branch44.html
### 5. Routes to ProjectBoard and AddProjectTask - branch45
### 5.1 branch45.html
### 6. AddProjectTask action ( )path) AddProjectTask form controlled part 1 -branch46
### 6.1 branch46.html
### 7. AddProjectTask action ( )path) AddProjectTask form controlled part 2 -branch47
### 7.1 branch47.html
### 8. Finish AddProjectTask action, handle errors part3 - branch48
### 8.1 branch48.html
### 9. Set up ProjectBoard, Backlog, ProjectTask components - branch49
### 9.1 branch49.html
## 6. Secure our App Spring Security + JWT
### 1. Intro to Spring Security Section
### 10. Token Generated!!! - branch65
### 10.1 branch65.html
### 11. Custom JWT filter to use our tokens - branch66
### 11.1 branch66.html
### 12. One User to Many Projects - branch67
### 12.1 branch67.html
### 13. Lock operations to specific User (Read and Delete) - branch68
### 13.1 branch68.html
### 14. Lock operations to specific User (Update) - branch69
### 14.1 branch69.html
### 15. User specific Create and Read Ops for Project Tasks - branch70
### 15.1 branch70.html
### 16. Find, Update, Delete  Project task with Security - branch71
### 16.1 branch71.html
### 2. IMPORTANT New to Spring Security.html
### 3. IMPORTANT New to JWTs.html
### 4. Initial Security Config - branch59
### 4.1 branch59.html
### 5. Create User Object, Validation, Repository, Service - branch60
### 5.1 branch60.html
### 6. User registration part 1 - branch61
### 6.1 branch61.html
### 7. User registration part 2 - branch62
### 8. User registration part 3 - branch63
### 8.1 branch63.html
### 9. JWT Provider pre-work - branch64
### 9.1 branch64.html
## 7. Secure our React App
### 1. Intro to Securing the React App, Security Components -branch72
### 1.1 branch72.html
### 10. SecuredRoutes - branch81
### 10.1 branch81.html
### 11. Bug Fixes
### 11.1 bug fixes commit - 8c3fefb.html
### 2. User registration happy path - branch73
### 2.1 branch73.html
### 3. User registration with validation- branch74
### 3.1 branch74.html
### 4. SecurityActions and SecurityReducer - branch75
### 4.1 branch75.html
### 5. Login form - branch76
### 5.1 branch76.html
### 6. Handle Login logic - branch77
### 6.1 branch77.html
### 7. Handle routing for expired token - branch78
### 7.1 branch78.html
### 8. Dynamic header based on security state - branch79
### 8.1 branch79.html
### 9. Lock public routes when logged in - branch80
## 8. Deploy to Heroku
### 1. MUST READ REQUIREMENTS FOR THIS SECTION.html
### 2. Step 1 - Connect Spring boot api to Clear DB
### 3. YOU NEED THIS FOR STEP 2.html
### 4. Step 2 - Deploy the Back-end to Heroku
### 5. Step 3 - Deploy with React build
### 6. POLYFILL CDN FOR STEP 4.html
### 7. Step 4 - Fix app to work with Internet explorer 11