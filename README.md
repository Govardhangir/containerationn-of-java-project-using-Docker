# 🐳 Containerization of Java Project using Docker

This project demonstrates how a **Java application** can be **containerized using Docker**, enabling it to run seamlessly across any environment — from local systems to production servers.  
It focuses on the **concept, architecture, and process** of containerization rather than only the commands.

---

## 📘 Table of Contents

- [Overview](#overview)
- [Project Objective](#project-objective)
- [Architecture](#architecture)
- [Project Flow](#project-flow)
- [Technologies Used](#technologies-used)
- [Outputs](#outputs)
- [Key Takeaways](#key-takeaways)
- [Author](#author)

---

## 🧩 Overview

Traditionally, Java applications often suffer from **“works on my machine”** problems due to inconsistent environments.  
Docker solves this challenge by packaging applications with their **runtime, dependencies, and libraries** inside lightweight containers.

This project shows how a Java application can be:

1. Built into a Docker image  
2. Tested in an isolated container environment  
3. Shared via **Docker Hub** for universal access and deployment  

---

## 🎯 Project Objective

The primary goals of this project are to:

- Understand **containerization** for Java-based applications  
- Ensure **consistent and reproducible deployments** across environments  
- Simplify integration with **CI/CD pipelines** and DevOps workflows  
- Gain hands-on understanding of **Docker architecture and image lifecycle**  

---

## 🏗️ Architecture

The containerization workflow is structured into a **three-stage architecture**:

### 🔹 1. Source Stage
- Prepare the Java project source files (`Main.java`, `pom.xml`, etc.)  
- Write a **Dockerfile** to define the base image, dependencies, and build process  

### 🔹 2. Build Stage
- Use Docker to build an image using a Java base (e.g., `openjdk:11`)  
- Compile and package the source code into a runnable `.jar` file  

### 🔹 3. Test & Deployment Stage
- Run the application in a container to validate functionality  
- Push the verified image to **Docker Hub** for reuse or deployment  

📊 **Architecture Diagram:**  
*(Upload this image in your repo and replace the link below)*  
![Architecture](images/architecture.png)

---

## ⚙️ Project Flow

```text
 ┌──────────────────────────────┐
 │   Java Source Code (App)    │
 └──────────────┬──────────────┘
                │
                ▼
 ┌──────────────────────────────┐
 │      Dockerfile Created      │
 │ (Defines build environment)  │
 └──────────────┬──────────────┘
                │
                ▼
 ┌──────────────────────────────┐
 │     Docker Image Built       │
 │ (Contains Java + App + Libs) │
 └──────────────┬──────────────┘
                │
                ▼
 ┌──────────────────────────────┐
 │   Container Runs the App     │
 │ (Isolated, Portable Runtime) │
 └──────────────┬──────────────┘
                │
                ▼
 ┌──────────────────────────────┐
 │    Image Stored on Docker    │
 │          Hub/Registry        │
 └──────────────────────────────┘


