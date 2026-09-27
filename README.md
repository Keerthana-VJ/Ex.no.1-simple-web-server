# Ex 01 - Simple Web Server using Spring Boot

## Name: Keerthana V
## Register Number: 212223220045

## AIM

To develop a simple web server using Spring Boot that can handle basic HTTP requests and return appropriate responses through RESTful endpoints.

---

## ALGORITHM

### Step 1: Create a New Spring Boot Project

1. Go to [Spring Initializr](https://start.spring.io/).
2. Create a new Maven project.
3. Select **Spring Web** as the dependency.
4. Generate and download the project.

### Step 2: Create the Main Application Class

Create the main application class with the `@SpringBootApplication` annotation.

This class contains the `main()` method, which starts the Spring Boot application.

### Step 3: Create a Controller Class

Create a controller class using the `@RestController` annotation.

The controller is responsible for handling HTTP requests and returning responses.

### Step 4: Define the Endpoint

Use the `@GetMapping` annotation to define a GET endpoint.

For this experiment, the endpoint is:

```text
GET /hello
```
The endpoint returns:
```text
Hello, Spring Boot!
```

### Step 5: Run the Application
Run the Spring Boot application using the IDE or Maven:
```
mvn spring-boot:run
```
Or, using the Maven wrapper:
```
./mvnw spring-boot:run
```

### Step 6: Test the Endpoint

Open a web browser or Postman and visit:

```http://localhost:8080/hello```

The following response should be displayed:
```text
Hello, Spring Boot!
```
### Step 7: Stop the Server

Stop the Spring Boot application after testing the endpoint.

## PROJECT STRUCTURE

simple-web-server/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── com/
│       │       └── example/
│       │           └── demo/
│       │               ├── DemoApplication.java
│       │               └── HelloController.java
│       │
│       └── resources/
│           └── application.properties
│
└── pom.xml

## PROGRAM

1. pom.xml
```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>4.1.1</version>
        <relativePath/> <!-- lookup parent from repository -->
    </parent>
    <groupId>com.example</groupId>
    <artifactId>Exp1</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <name>Exp1</name>
    <description>Exp1</description>
    <url/>
    <licenses>
        <license/>
    </licenses>
    <developers>
        <developer/>
    </developers>
    <scm>
        <connection/>
        <developerConnection/>
        <tag/>
        <url/>
    </scm>
    <properties>
        <java.version>17</java.version>
    </properties>
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-webmvc</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-webmvc-test</artifactId>
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

2. Exp1Application.java
```
package com.example.exp1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Exp1Application {

    public static void main(String[] args) {
        SpringApplication.run(Exp1Application.class, args);
    }

}
```

3.  HelloController.java
```
package com.example.exp1;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {
    @GetMapping("/hello")
    public String hello(){
        return "Hello, Spring Boot!";
    }
}
```

## OUTPUT

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0d819a6c-66cf-430e-b083-13594c0d5bcd" />

## RESULT
Thus the Spring Boot application with a REST controller that returns "Hello, Spring Boot!" when accessed via  GET- /hello was created and executed successfully. 
