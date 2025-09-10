# 🏦 Bank Management System

A **Spring Boot** project for managing bank operations like user accounts, transactions, and authentication using **Spring Security** and **JWT**.  
This project uses **MySQL** as the database and follows modern practices with Spring Boot 3 and Java 21.

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
![Java](https://img.shields.io/badge/Java-21-red?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2-brightgreen?logo=springboot)
![MySQL](https://img.shields.io/badge/MySQL-8.0-blue?logo=mysql)
![Maven](https://img.shields.io/badge/Maven-3.9-orange?logo=apachemaven)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Build](https://img.shields.io/badge/Build-Passing-success?logo=githubactions)

## 📂 Project Structure
bank-management-system/
┣ 📂 src/main/java/com/alien/bank
┃ ┣ 📂 controller # REST Controllers
┃ ┣ 📂 model # Entities (JPA)
┃ ┣ 📂 repository # JPA Repositories
┃ ┣ 📂 service # Business Logic
┃ ┗ 📜 BankManagementSystemApplication.java
┣ 📂 src/main/resources
┃ ┣ 📜 application.properties (or application.yml)
┃ ┗ 📜 schema.sql / data.sql (optional)
┣ 📜 pom.xml
┗ 📜 README.md

yaml
Copy code


🏗️ Architecture
📦 Bank Management System
├── 📂 config/          # Application configuration
├── 📂 controller/      # REST API controllers
├── 📂 entity/          # JPA entities
├── 📂 exception/       # Custom exception handling
├── 📂 mapper/          # Data mapping utilities
├── 📂 model/           # Data transfer objects
├── 📂 repository/      # Data access layer
├── 📂 security/        # Security configurations
├── 📂 service/         # Business logic layer
└── 📂 utils/           # Utility classes
 licensed under the MIT License - see the LICENSE file for details.
