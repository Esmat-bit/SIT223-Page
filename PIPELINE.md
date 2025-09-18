# SIT223-753 Jenkins Pipeline (Part 1 – Task 1)

This document describes the design of a Jenkins pipeline that integrates with GitHub.  
The pipeline is triggered automatically when new commits are pushed (via SCM polling).  
It consists of **7 stages**, each performing a specific task.

---

## Stage 1: Build
- **Task**: Compile and package the source code.  
- **Tool**: Maven (for Java projects) or Gradle.  

---

## Stage 2: Unit and Integration Tests
- **Task**: Run automated unit tests to validate functions, and integration tests to check how components interact.  
- **Tools**: JUnit (Java), Mocha/Chai (Node.js), PyTest (Python).  

---

## Stage 3: Code Analysis
- **Task**: Perform static code analysis to ensure code quality and compliance with industry standards.  
- **Tool**: SonarQube or Checkstyle.  

---

## Stage 4: Security Scan
- **Task**: Identify vulnerabilities in dependencies and code.  
- **Tool**: OWASP Dependency-Check or Snyk.  

---

## Stage 5: Deploy to Staging
- **Task**: Deploy the built application to a staging server for further testing.  
- **Tools**: Jenkins SSH plugin, Ansible, or AWS EC2.  

---

## Stage 6: Integration Tests on Staging
- **Task**: Validate the application in a staging (production-like) environment.  
- **Tools**: Selenium (UI testing), Postman (API testing).  

---

## Stage 7: Deploy to Production
- **Task**: Release the final build to production servers.  
- **Tools**: Ansible, AWS CodeDeploy, Jenkins SSH plugin.  

---
