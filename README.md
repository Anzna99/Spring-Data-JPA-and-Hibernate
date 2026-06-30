# Spring-Data-JPA-and-Hibernate
COGNIZANT DEEP SKILLING 
# ORM Learn – Spring Data JPA and Hibernate

## Overview

This project demonstrates the use of Spring Boot, Spring Data JPA, Hibernate, and MySQL for performing database operations on a Country table.

## Technologies Used

* Java 17
* Spring Boot
* Spring Data JPA
* Hibernate
* MySQL 8.0
* Maven

## Project Structure

src/main/java

* com.cognizant.ormlearn

  * OrmLearnApplication.java
* com.cognizant.ormlearn.model

  * Country.java
* com.cognizant.ormlearn.repository

  * CountryRepository.java
* com.cognizant.ormlearn.service

  * CountryService.java

src/main/resources

* application.properties

## Database Setup

Create the database schema:

```sql
CREATE SCHEMA ormlearn;
```

Create the Country table:

```sql
CREATE TABLE country(
    co_code VARCHAR(2) PRIMARY KEY,
    co_name VARCHAR(50)
);
```

Insert sample records:

```sql
INSERT INTO country VALUES ('IN', 'India');
INSERT INTO country VALUES ('US', 'United States of America');
```

## Configuration

Update the database credentials in application.properties if required:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ormlearn
spring.datasource.username=root
spring.datasource.password=root
```

## Build the Project

```bash
mvn clean install
```

## Run the Application

```bash
mvn spring-boot:run
```

## Features Implemented

* Spring Boot Application
* JPA Entity Mapping
* Repository Layer using JpaRepository
* Service Layer with @Transactional
* Hibernate Integration
* MySQL Connectivity
* Logging using SLF4J

## Expected Output

The application fetches all countries from the database and prints them in the application logs.

Example:

```text
Country [code=IN, name=India]
Country [code=US, name=United States of America]
```

## Author

Prepared as part of the Spring Data JPA and Hibernate Hands-on Exercise.
