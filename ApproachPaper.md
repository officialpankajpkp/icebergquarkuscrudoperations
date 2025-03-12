# Approach Paper: Iceberg Quarkus CRUD Operations

## Table of Contents

1. [Objective](#objective)  
2. [Proposed Solutions](#proposed-solutions)  
3. [Approach 1: Podman-Based Deployment](#approach-1-podman-based-deployment) 
   - [Flow Chart](#flow-chart) 
   - [Architecture Diagram](#architecture-diagram)  
   - [Description](#description)  
   - [Pre-requisites](#pre-requisites)  
     - [Hardware Requirements](#hardware-requirements)  
     - [Software Requirements](#software-requirements)  
     - [Networking Requirements](#networking-requirements)  
4. [Approach 2: Kubernetes-Based Deployment](#approach-2-kubernetes-based-deployment)  
   - [Architecture Diagram](#architecture-diagram-1)  
   - [Description](#description-1)  
   - [Pre-requisites](#pre-requisites-1)  
     - [Hardware Requirements](#hardware-requirements-1)  
     - [Software Requirements](#software-requirements-1)  
     - [Networking Requirements](#networking-requirements-1)  

---

## Objective

The goal of this project is to set up **Apache Iceberg** using **Podman**, integrate **Trino** for SQL query execution, and develop a **Java Quarkus** application to provide a user-friendly interface for database interactions.

## Proposed Solutions

There are two possible approaches for implementing this solution:

1. **Deploying Iceberg and Trino using Podman** to keep the setup lightweight and secure.  
2. **Using Kubernetes** to manage the containerized environment for better scalability and automation.  

### Chosen Approach: Approach 1 (Podman-Based Deployment)

#### *Why This Approach?*

-  Simpler setup and management compared to Kubernetes.  
-  Better security with rootless Podman containers.  
-  Fits current project requirements while allowing room for future scaling if needed.  

This approach is the most practical for our current use case, ensuring a balance between **efficiency, security, and ease of deployment**. Further refinements will be made as the project progresses.

---

## Approach 1: Podman-Based Deployment

### Flow Chart

![Flow Chart](https://github.com/officialpankajpkp/icebergquarkuscrudoperations/blob/review1/Flow%20chart%202%20project.png)
 

### Architecture Diagram

![Architecture Diagram](https://github.com/officialpankajpkp/icebergquarkuscrudoperations/blob/review1/Architecture%20Diagram1.png)  

### Description

In this approach, **Apache Iceberg** and **Trino** are deployed as containerized services using **Podman**. The **Java Quarkus** application will interact with **Trino**, which in turn will query **Iceberg tables**.

#### *Pros:*
-  Easier to set up and manage compared to Kubernetes.  
-  Podman offers improved security as it runs in rootless mode.  
-  No need for additional orchestration tools.  

#### *Cons:*
-  Not as scalable as a Kubernetes-based solution.  
-  Requires manual handling of container lifecycles.  

### Pre-requisites

#### *Hardware Requirements*
- **Minimum 16GB RAM**  
- **Multi-core processor (Intel i5 or higher)**  
- **At least 100GB disk space**  

#### *Software Requirements*
- **Podman (v4.x or later)**  
- **Apache Iceberg (latest release)**  
- **Trino (v414+)**  
- **Java Quarkus (v3.x)**  
- **PostgreSQL (if using a catalog service)**  

#### *Networking Requirements*
-  **Open ports**: `8080 (Quarkus)`, `9090 (Trino UI)`, `1527 (PostgreSQL, if used)`  
-  **Internet access for fetching container images**  

---

## Approach 2: Kubernetes-Based Deployment

### Architecture Diagram

*(Diagram to be added here)*  

### Description

This approach involves deploying **Iceberg** and **Trino** as **Kubernetes-managed services**, leveraging Kubernetes features like **orchestration, service discovery, and scaling**.

#### *Pros:*
- Well-suited for large-scale deployments.  
- Provides automated scaling and self-healing capabilities.  
- Easier management of containerized workloads.  

#### *Cons:*
- More complex to set up and maintain.  
- Requires Kubernetes expertise and cluster management.  

### Pre-requisites

#### *Hardware Requirements*
- **Minimum 32GB RAM (for Kubernetes nodes)**  
- **Multi-core processor (Intel i7 or higher)**  
- **At least 250GB disk space**  

#### *Software Requirements*
- **Kubernetes (v1.25+)**  
- **Helm (for managing deployments)**  
- **Apache Iceberg (latest release)**  
- **Trino (v414+)**  
- **Java Quarkus (v3.x)**  
- **PostgreSQL (if using a catalog service)**  

#### *Networking Requirements*
- **Open ports**: `8080 (Quarkus)`, `9090 (Trino UI)`, `1527 (PostgreSQL, if used)`  
- **Kubernetes ingress configuration for external access**  


