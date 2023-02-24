# Resgistration_Login_Module

# Resgistration_Login_Module


This is application is developed to perform registration, login, and logout features using Spring boot, Spring Security, Spring Data JPA, Thymeleaf, and the MySQL database.

#Backend Development

First I have created database in MySQL : then with the help of code created tables as user and role 
![image](https://user-images.githubusercontent.com/125120045/221257183-0704488b-fd25-4a90-bde2-a700f576d902.png)



then I have added required dependencies into po.xml file for mysql connector
added thymleaf depedencies with compatible version.

In application.properties file i have added details regarding mysqldatabase ::

spring.datasource.url=jdbc:mysql://localhost:3306/userdetails?useSSL=false
spring.datasource.username=root
spring.datasource.password=root

spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQL5InnoDBDialect

spring.jpa.hibernate.ddl-auto=update

logging.level.org.hibernate.SQL=DEBUG
logging.level.org.hibernate.type=TRAC


To create Tables in database created two entity classes : see class files Role.java and User.java

used JPA repository as a API for storing and retriving data from the database: see class file UserRepository.java

To provide security to the application , have used  WebSecurityConfigurerAdapter : see class file SecurityConfiguration.java


#Frontend Developement

So for frontend I have used Thymeleaf as a server-side Java template engine
have created HTML pages for  main index page,registration and  main index page using CSS and bootstrap to give look to the application
see the html files under resource folder 
index.html
login.html
registration.html

So after started my application on 8080 port

so in browser when I hit this url :: http://localhost:8080/index.html

it gives following window
![image](https://user-images.githubusercontent.com/125120045/221260557-117e4c69-85e6-4d06-b4e7-cb885f585017.png)

then if we are new user we can select "Register Here"
otherwise can signup with our credentials

suppose we clicked on "Register here"

then below page will get opened , here we can register ourself for the application, I have registered myself here
![image](https://user-images.githubusercontent.com/125120045/221261798-c5346036-e6d2-477a-9219-8d14ab6a302b.png)

I got message of success as follows:
![image](https://user-images.githubusercontent.com/125120045/221262423-3bd16a5f-91d6-4d19-96e1-6cafb5821bdf.png)

so my data get stored in database: so when I fetch the details from User table I get below data 

when we click login here from registration page it will go to login page (see the second image)

So when I login with my crendiatls , like this ![image](https://user-images.githubusercontent.com/125120045/221263897-f0faafbe-8934-4b69-bd15-712053e713a2.png)

it will give us login successful message with WelcomeUsername and also logout button is there to logout 
like this ![image](https://user-images.githubusercontent.com/125120045/221266183-6ced58e5-6203-40ab-a508-3b4dd81e1e2c.png)


