# Spring Cloud Gateway Example

## Overview

This project demonstrates how to build an **API Gateway** using **Spring Cloud Gateway** in a microservices architecture.

An API Gateway acts as the **single entry point** for all client requests. Instead of clients calling multiple services directly, they send requests to the gateway, which then routes the request to the appropriate backend service.

Spring Cloud Gateway provides **routing, filtering, security, monitoring, and load balancing** capabilities for microservices.

This project is created to understand the **Gateway pattern and reactive request routing using Spring WebFlux**.

---

## Architecture

Client
↓
API Gateway (Spring Cloud Gateway)
↓
Microservices

The gateway receives requests from the client and routes them to the correct backend service based on predefined routing rules.

---

## Features

* API Gateway implementation using **Spring Cloud Gateway**
* Centralized entry point for microservices
* **Dynamic request routing**
* **Path-based routing**
* Reactive architecture using **Spring WebFlux**
* Easy integration with microservices
* Scalable architecture for distributed systems

---

## Tech Stack

* **Java**
* **Spring Boot**
* **Spring Cloud Gateway**
* **Spring WebFlux**
* **Maven**
* **REST APIs**

---

## Project Structure

```
spring-cloud-gateway
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── (application source code)
│   │   │
│   │   └── resources
│   │       ├── application.yml / application.properties
│   │       └── configuration files
│   │
│   └── test
│
├── pom.xml
│
└── README.md
```

---

## How It Works

1. A client sends a request to the **API Gateway**.
2. The gateway inspects the **request path**.
3. Based on configured routes, the request is forwarded to the appropriate service.
4. The microservice processes the request and returns a response.
5. The gateway forwards the response back to the client.

This approach helps simplify client interactions with multiple backend services.

---

## Example Routing

Example request from client:

```
http://localhost:8080/service1/api
```

Gateway route configuration:

```
/service1/** → forwards to Service 1
/service2/** → forwards to Service 2
```

The gateway automatically forwards the request to the appropriate backend service.

---

## Running the Project

### Prerequisites

Make sure you have the following installed:

* Java 17 or later
* Maven
* IDE (IntelliJ / VS Code / Eclipse)

---

### Clone the Repository

```
git clone https://github.com/aryanguptaa001/spring-cloud-gateway.git
cd spring-cloud-gateway
```

---

### Build the Project

```
mvn clean install
```

---

### Run the Application

```
mvn spring-boot:run
```

The API Gateway will start at:

```
http://localhost:8080
```

---

## Use Cases of API Gateway

API Gateway is widely used in **microservices architectures** to:

* Provide a **single entry point** for clients
* Handle **authentication and authorization**
* Perform **load balancing**
* Implement **rate limiting**
* Provide **logging and monitoring**
* Simplify client communication with multiple services

---

## Learning Objectives

Through this project, the following concepts can be understood:

* Microservices architecture
* API Gateway pattern
* Reactive programming with Spring WebFlux
* Request routing and filtering
* Building scalable distributed systems

---

## Future Improvements

Possible enhancements for this project include:

* Adding **JWT authentication**
* Integrating **service discovery (Eureka)**
* Implementing **rate limiting**
* Adding **logging and monitoring**
* Integrating **Resilience4j circuit breaker**

---

## Author

Aryan Gupta

Backend Developer (Java | Spring Boot | Microservices)

GitHub: https://github.com/aryanguptaa001
