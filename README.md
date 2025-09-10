# 🏦 Bank Management System

A **Spring Boot** project for managing bank operations like user accounts, transactions, and authentication using **Spring Security** and **JWT**.  
This project uses **MySQL** as the database and follows modern practices with Spring Boot 3 and Java 21.

---


---
![Java](https://img.shields.io/badge/Java-21-red?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2-brightgreen?logo=springboot)
![MySQL](https://img.shields.io/badge/MySQL-8.0-blue?logo=mysql)
![Maven](https://img.shields.io/badge/Maven-3.9-orange?logo=apachemaven)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Build](https://img.shields.io/badge/Build-Passing-success?logo=githubactions)

## 📂 Project Structure

bank-management-system/
┣ 📂 src/main/java/com/alien/bank/management/system
┃ ┣ 📂 config # Configuration classes (e.g., security, beans)
┃ ┣ 📂 controller # REST controllers (API endpoints)
┃ ┣ 📂 entity # JPA entities
┃ ┣ 📂 exception # Custom exceptions & handlers
┃ ┣ 📂 mapper # DTO ↔ Entity mappers (e.g., MapStruct / manual)
┃ ┣ 📂 model # DTOs / Request & Response models
┃ ┣ 📂 repository # JPA repositories (interfaces extending JpaRepository)
┃ ┣ 📂 security # Security-related classes (filters, JWT, config)
┃ ┣ 📂 service # Service layer (business logic)
┃ ┣ 📂 utils # Utility/helper classes
┃ ┣ 📜 ApplicationConfig.java
┃ ┗ 📜 BankManagementSystemApplication.java
┣ 📂 src/main/resources
┃ ┣ 📜 application.properties (or application.yml)
┃ ┗ 📜 schema.sql / data.sql (optional for DB init)
┣ 📂 src/test/java/com/alien/bank/management/system
┃ ┗ 📂 (same structure as main for tests)
┣ 📜 pom.xml
┗ 📜 README.md


---

## 🚀 Tech Stack
- **Java 21**
- **Spring Boot 3.x**
- **Spring Security + JWT**
- **Spring Data JPA (Hibernate)**
- **MySQL**
- **Lombok**
- **Swagger / OpenAPI** for API documentation

---

## ⚙️ Configuration

In `src/main/resources/application.properties` configure MySQL:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/bankdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

▶️ Running the Project
Using Maven
mvn spring-boot:run

Or build a jar
mvn clean package
java -jar target/bank-management-system-0.0.1-SNAPSHOT.jar

