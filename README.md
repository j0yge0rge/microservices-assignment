# Microservices Architecture Report

**Course:** Software Architecture
**Student:** Joy George
**Date:** April 2026

---

## 📌 Introduction

This project demonstrates a simple microservices architecture using two independent Spring Boot services communicating via HTTP and containerized using Docker.

---

## ⚙️ System Overview

The system consists of:

* **Service A** (Client Service): Sends requests
* **Service B** (Data Service): Provides responses

The services are connected using docker-compose and communicate over REST APIs.

---

## 🚀 Benefits of Microservices

This lab highlights several advantages of microservices over a monolithic architecture. Each service operates independently, allowing for better modularity and flexibility. Developers can update or redeploy one service without affecting the other.

Additionally, fault isolation is demonstrated—when Service B fails, Service A continues running and handles the failure gracefully.

---

## ⚠️ Complexities Introduced

Splitting the system introduces additional complexity. Services must communicate over a network, which requires handling HTTP requests and possible failures.

Deployment also becomes more complex since multiple services must be built, configured, and run together using Docker and docker-compose. Debugging is harder because issues can occur across different services.

---

## ⏱️ Impact of Latency and Failures

If network latency increases or Service B becomes slow, Service A will experience delays. This can lead to slow responses or timeouts.

In the failure simulation, when Service B is stopped, Service A cannot retrieve data and returns an error message. This demonstrates how microservices depend on reliable inter-service communication.

---

## 🧩 12-Factor App Principles

This implementation reflects several 12-factor app principles:

* **Independent services**: Each service runs separately
* **Statelessness**: No shared state between requests
* **Port binding**: Each service exposes a port
* **Environment-based configuration**: Docker manages runtime setup
* **Scalability**: Services can be scaled independently

---

## 📸 Screenshots

Refer to the `/screenshots` folder for:

* Successful API communication
* Failure simulation

---

## ✅ Conclusion

This project demonstrates how microservices improve modularity and scalability while introducing challenges such as network dependency and deployment complexity.

---
