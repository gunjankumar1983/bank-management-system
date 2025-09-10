# 🏦 Bank Management System  

A *Spring Boot* project for managing bank operations like user accounts, transactions, and authentication using *Spring Security* and *JWT*.  
It uses *MySQL* as the database and follows modern practices with *Spring Boot 3* and *Java 21*.  


| Java 21 | Spring Boot 3.x | MySQL 8.0 | Maven 3.9 | Build: Passing | License: MIT |
|:-------:|:---------------:|:---------:|:---------:|:--------------:|:------------:|
| ![Java](https://img.shields.io/badge/Java-21-red?logo=openjdk) | ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2-brightgreen?logo=springboot) | ![MySQL](https://img.shields.io/badge/MySQL-8.0-blue?logo=mysql) | ![Maven](https://img.shields.io/badge/Maven-3.9-orange?logo=apachemaven) | ![Build](https://img.shields.io/badge/Build-Passing-success?logo=githubactions) | ![License](https://img.shields.io/badge/License-MIT-yellow) |


---

## 📂 Project Structure  


```bank-management-system/
 ┣ 📂 src/main/java/com/alien/bank/management/system
 ┃ ┣ 📂 config        # Configuration classes (security, beans, etc.)
 ┃ ┣ 📂 controller    # REST API controllers
 ┃ ┣ 📂 entity        # JPA entities
 ┃ ┣ 📂 exception     # Custom exceptions and handlers
 ┃ ┣ 📂 mapper        # DTO ↔ Entity mappers
 ┃ ┣ 📂 model         # DTOs (Request & Response)
 ┃ ┣ 📂 repository    # Data access (JpaRepository interfaces)
 ┃ ┣ 📂 security      # Authentication & Authorization (JWT, filters)
 ┃ ┣ 📂 service       # Business logic layer
 ┃ ┣ 📂 utils         # Utility/helper classes
 ┃ ┗ 📜 BankManagementSystemApplication.java
 ┣ 📂 src/main/resources
 ┃ ┣ 📜 application.properties (Spring configuration)
 ┃ ┗ 📜 schema.sql / data.sql (optional DB init)
 ┣ 📂 src/test/java/... (unit & integration tests)
 ┣ 📜 pom.xml
 ┗ 📜 README.md```


---

## 🚀 Tech Stack  

- Java 21  
- Spring Boot 3.x  
- Spring Security + JWT  
- Spring Data JPA (Hibernate)  
- MySQL  
- Lombok  
- Swagger / OpenAPI (API documentation)  

---

## 🎯 Features  

### 👤 Account Management  
- Create and manage customer accounts  
- KYC verification & multiple account types  
- Account status management  

### 💳 Transaction Services  
- Real-time money transfers  
- Transaction history & tracking  
- Balance checks  
- Transaction limits & validation  

### 🔒 Security  
- JWT-based authentication  
- Role-based access control  
- AES-256 encrypted storage  
- Audit logging & activity monitoring  

### 📈 Reporting & Analytics  
- Transaction reports  
- Account statements  
- Administrative dashboards  
- Export functionality  

---

## ⚡ Getting Started  

### Prerequisites  
- ☕ Java 17+  
- 📦 Maven 3.6+  
- 🗄 MySQL 8.0+  
- 🔧 Git  

### Installation  


# Clone the repository
git clone https://github.com/yourusername/bank-management-system.git
cd bank-management-system

# Install dependencies
mvn clean install

# Run the application
mvn spring-boot:run


The application will start at:  
👉 [http://localhost:8080](http://localhost:8080)

---

## ⚙ Configuration  

Update application.properties with your DB and JWT configs:  


# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/bank_management_db
spring.datasource.username=bank_user
spring.datasource.password=your_password

# JPA Settings
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# Server Port
server.port=8080

# JWT Configuration
jwt.secret=your-secret-key
jwt.expiration=86400000


---

## 📚 API Endpoints  

### 🔑 Authentication  
- POST /api/auth/login  
- POST /api/auth/register  
- POST /api/auth/refresh  

### 👤 Account Management  
- GET /api/accounts  
- POST /api/accounts  
- GET /api/accounts/{id}  
- PUT /api/accounts/{id}  
- DELETE /api/accounts/{id}  

### 💳 Transactions  
- GET /api/transactions  
- POST /api/transactions/transfer  
- GET /api/transactions/{id}  
- GET /api/transactions/account/{accountId}  

---

## 🧪 Testing  

Run all tests:  

mvn test


Generate coverage report:  

mvn jacoco:report


---

## 🚀 Deployment  

### 🐋 Docker  


FROM maven:3.8-openjdk-21 AS build
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package

FROM openjdk:21-jre-slim
WORKDIR /app
COPY --from=build /app/target/*.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]


Build & Run with Docker:  

docker build -t bank-management-system .
docker run -p 8080:8080 bank-management-system


---

## 🤝 Contributing  

1. Fork the repo  
2. Create a feature branch (git checkout -b feature/new-feature)  
3. Commit changes (git commit -m "Add new feature")  
4. Push (git push origin feature/new-feature)  
5. Create a Pull Request  
```
