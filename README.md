# kodilla-html-css-js

![HTML](https://img.shields.io/badge/HTML-5-orange)
![CSS](https://img.shields.io/badge/CSS-3-blue)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)
![SpringBoot](https://img.shields.io/badge/Backend-SpringBoot-green)
![Gradle](https://img.shields.io/badge/Gradle-8-green)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

This repository contains exercises, homework assignments, and a simple full-stack project created as part of a module in the **Kodilla "Automated Tester" Java course**, focusing on **HTML, CSS and JS**.

It includes:

- standalone HTML/CSS/JS exercises
- a complete tasks frontend
- a Spring Boot backend for handling tasks
- practice with DOM manipulation, events, AJAX calls, and API integration

The project was developed in **IntelliJ IDEA** as part of the learning path for future **QA/Test Automation Engineers**.

---

## Description

This module introduces frontend fundamentals and integrates them with a backend API.

### ✔ Frontend (HTML / CSS / JavaScript)
- webpage structure (HTML5)
- layouts and styling (CSS3)
- DOM manipulation
- event listeners
- forms and validation
- AJAX requests using jQuery
- dynamically rendered content
- interactive task application UI

### ✔ Backend – Spring Boot
Project located in: `projekt_js/tasks_app_backend/`

Backend provides:
- full CRUD operations for tasks
- REST controllers (`TaskController`, `TrelloController`)
- integration with an external API (Trello API simulation)
- DTO mapping layer
- service & repository layer
- database access via Spring Data JPA
- OpenAPI documentation (springdoc)

### ✔ Homework
Folder: `homework 12.3/`  
Contains:
- `index.html`
- `script.js`
- `style.css`

A standalone JS task demonstrating:
- event handling
- array manipulation
- UI updates

---

## Project Structure
```
kodilla-html-css-js/
│
├── homework 12.3/
│ index.html
│ script.js
│ style.css
│
├── projekt_js/
│ └── tasks_app_backend/
│ build.gradle
│ settings.gradle
│ gradlew / gradlew.bat
│
│ src/main/java/com/crud/tasks/
│ TasksApplication.java
│ config/CoreConfiguration.java
│
│ controller/
│ TaskController.java
│ TrelloController.java
│ TaskNotFoundException.java
│
│ domain/
│ Task.java
│ TaskDto.java
│ TrelloCardDto.java
│ TrelloBoardDto.java
│ ...
│
│ mapper/
│ TaskMapper.java
│ TrelloMapper.java
│
│ repository/
│ TaskRepository.java
│
│ service/
│ DbService.java
│ TrelloService.java
│
│ trello/
│ client/TrelloClient.java
│ config/TrelloConfig.java
│ facade/TrelloFacade.java
│ validator/TrelloValidator.java
│
│ src/test/java/com/crud/tasks/
│ TaskControllerTest.java
│ TrelloClientTest.java
│ TrelloFacadeTest.java
│ TaskMapperTestSuite.java
│ ...
│
└── task_app_frontend/
index.html
script.js
style.css
jquery-3.2.1.min.js
```

## Getting Started

Frontend can run standalone, but is designed to communicate with the backend REST API.

### Backend Dependencies (Gradle)

```gradle
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    implementation 'org.springframework.boot:spring-boot-starter-mail'
    implementation 'org.springframework.boot:spring-boot-starter-web'
    implementation 'org.springdoc:springdoc-openapi-starter-webmvc-ui:2.2.0'
    implementation 'com.google.code.gson:gson:2.10'

    compileOnly 'org.projectlombok:lombok'
    annotationProcessor 'org.projectlombok:lombok'

    runtimeOnly 'com.mysql:mysql-connector-j'

    testImplementation 'org.springframework.boot:spring-boot-starter-test'
    testRuntimeOnly 'org.junit.platform:junit-platform-launcher'
}
```
Backend provides:
- REST API for tasks
- JSON serialization via Gson
- API documentation on http://localhost:8080/swagger-ui.html
---

## Test Suites Overview
✔ **Controller Tests**

Validate REST endpoints for:
- task CRUD operations
- Trello controller integration
- exception handling (TaskNotFoundException)

Files:
- TaskControllerTest
- TrelloControllerTest

✔ **Mapper Tests**
- Ensure DTO ↔ entity conversion:
- TaskMapperTestSuite
- TrelloMapperTestSuite

✔ **Service Layer Tests**

Focus on:
- database operations
- behaviors
- service logic

Files:
- DbServiceTestSuite

✔ **Trello Client/Facade Tests**

Validate:
- API communication layer
- filtering, validation and processing logic

Files:
- TrelloClientTest
- TrelloFacadeTest
---

## Running the Projects
✅ Frontend (standalone)

Simply open:
```bash
task_app_frontend/index.html
```

or for homework:
```bash
homework 12.3/index.html
```

✅ Backend (Spring Boot)

Linux/macOS
```bash
./gradlew bootRun
```

Windows
```bash
gradlew bootRun
```

Backend runs at:
```
http://localhost:8080
```

Available Swagger UI:
```
http://localhost:8080/swagger-ui.html
```
---
## Optional Terminal Commands

Build backend
```bash
./gradlew build
```

Run tests
```bash
./gradlew test
```

Clean
```bash
./gradlew clean
```

---
## Authors

Created by:

**Joanna Kamińska**  
GitHub: https://github.com/joanna-kaminska-qa

---

## Version History

- **0.2** – README added, improved structure
- **0.1** – Initial upload

---

## License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for details.

---

## Acknowledgments

- Kodilla Automated Tester Java course
- MDN Web Docs (HTML/CSS/JS)
- jQuery documentation
- Spring Boot documentation
- OpenAPI / Swagger
