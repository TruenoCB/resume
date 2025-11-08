---
permalink: /
title: "About Me"
excerpt: "Distributed Storage Engineer with 2+ years of expertise in object storage, image storage, and high-performance distributed systems at JD.com"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

### Professional Overview
Results-driven Distributed Storage Engineer with **2+ years of hands-on experience** designing, developing, and optimizing mission-critical storage systems at JD.com. Specializing in **object storage, image storage, and distributed data persistence** for high-concurrency e-commerce scenarios. Pursuing a Master's degree in Software Engineering with a strong academic background in distributed systems, cloud-native technologies, and data consistency protocols. Proven track record of improving system performance, reducing costs, and enhancing reliability through technical innovation and engineering best practices.

### Core Technical Skills
- **Programming Languages**: Golang (Proficient, 2+ years), Java (Familiar, 3+ years), SQL/NoSQL, Shell Scripting
- **Storage Technologies**: Object Storage (MinIO/S3-compatible), Image Storage Optimization, Distributed File Systems, Tiered Storage (SSD/HDD)
- **Databases & Middleware**: MySQL (Index Tuning/Transaction), Redis Cluster (Distributed Lock/Persistence), Kafka (Async Data Pipeline)
- **Distributed Systems**: Raft/Paxos Consistency, Data Replication, Fault Tolerance, Load Balancing, Distributed Lock
- **Cloud-Native & DevOps**: Docker, Kubernetes, Helm, CI/CD (Jenkins/GitLab CI), Infrastructure as Code
- **Monitoring & Observability**: Prometheus, Grafana, ELK Stack, Custom Metrics Exporters
- **Foundations**: TCP/IP Protocol, Concurrency Control (GMP/Threads), Data Structures & Algorithms, Performance Tuning

### Professional Experience
#### Distributed Storage Engineer | JD.com (Jul 2022 - Present)
**Team**: Core Storage Platform Department  
Responsible for designing and optimizing JD's flagship distributed storage platform, supporting object storage and image storage services that power JD's e-commerce, logistics, and marketing ecosystems (serving 100M+ daily active users).

- Led the development of a high-throughput image storage service for product detail pages and marketing campaigns, supporting **100M+ daily uploads/downloads** with 99.99% service availability.
- Optimized object storage metadata consistency based on the Raft protocol, reducing replication latency by 30% (from 150ms to 105ms) and lowering cross-region bandwidth consumption by 40%.
- Designed and implemented a distributed cache layer using Redis Cluster for hot image data, improving access performance by 400% (from 200ms to 40ms) and reducing origin server load by 60%.
- Executed cloud-native migration of legacy storage systems, leveraging Kubernetes for orchestration and dynamic resource scaling, cutting off-peak resource waste by 25%.
- Built end-to-end monitoring and alerting systems with Prometheus and Grafana, enabling real-time fault detection and reducing mean time to resolve (MTTR) by 50%.
- Implemented tiered storage strategy (hot data in SSD, cold data in HDD) and intelligent prefetching algorithms, reducing overall storage costs by 15% while maintaining SLA commitments.

### Key Projects
#### 1. GoFlow Async Task Processing Framework (Mar 2023 - Jul 2023)
- **Role**: Architecture Design & Core Development (Personal Project)
- **Objective**: Build a high-performance asynchronous task framework tailored for distributed storage scenarios (e.g., data backup, migration, and consistency checks).
- **Achievements**:
  - Designed a scalable two-tier architecture (flowsvr for task scheduling, worker for task execution) supporting horizontal scaling to 100+ nodes.
  - Optimized throughput from 500 QPS to 2000 QPS via MySQL connection pool tuning, Redis caching, and lock contention reduction.
  - Replaced MySQL row-level locks with Redis distributed locks, resolving multi-machine competition issues and reducing CPU usage by 35%.
  - Implemented dynamic task priority adjustment based on storage cluster load, ensuring critical tasks (e.g., disaster recovery) are prioritized.
- **Tech Stack**: Golang, MySQL, Redis, Protobuf, Docker, Gin

#### 2. Distributed Cache System & Web Framework (Dec 2022 - Feb 2023)
- **Role**: Independent Development (Personal Project)
- **Objective**: Develop a high-availability distributed cache system integrated with a lightweight web framework for storage service APIs.
- **Achievements**:
  - Implemented LRU cache algorithm with read-write locks for concurrency control, supporting 100K+ QPS per node.
  - Built service discovery and fault tolerance based on Etcd and Raft-like protocol, ensuring 99.9% cache cluster availability.
  - Applied consistency hash algorithm for uniform data distribution, enabling horizontal scaling without data migration.
  - Web framework supports dynamic routing, middleware (auth/monitoring), and context management for RESTful API development.
- **Tech Stack**: Golang, Etcd, Protobuf, LRU, Consistency Hash, Gin

### Contact & Portfolio
- Email: [trueno_cb@163.com](mailto:trueno_cb@163.com)
- GitHub: [github.com/TruenoCB](https://github.com/TruenoCB)
- Technical Blog: [trueno.cloud](https://www.trueno.cloud)
- Location: Beijing, China



### Key Projects

#### 1. GoFlow Async Task Processing Framework
**Duration**: Mar 2023 - Jul 2023  
**Role**: Architecture Design & Core Development (Personal Project)  
**Tech Stack**: Golang, MySQL, Redis, Protobuf, Docker, Kubernetes, Gin  

##### Project Overview
A high-performance asynchronous task processing framework designed specifically for distributed storage scenarios (e.g., data backup, migration, consistency checks, and batch processing). The framework enables developers to build scalable, fault-tolerant task workflows with minimal code.

##### Core Features
- **Scalable Architecture**: Two-tier design (flowsvr for task scheduling, worker for execution) supporting horizontal scaling to 100+ nodes.
- **Performance Optimization**:
  - Tuned MySQL connection pool (max connections, idle timeout) to handle high concurrent task metadata operations.
  - Implemented Redis caching for frequently accessed task data, reducing database load by 60%.
  - Reduced lock contention via fine-grained locking strategies, improving throughput from 500 QPS to 2000 QPS.
- **Distributed Coordination**:
  - Replaced MySQL row-level locks with Redis distributed locks to resolve multi-machine competition, reducing CPU usage by 35%.
  - Supported task sharding across workers to ensure load balancing.
- **Task Management**:
  - Dynamic priority adjustment based on storage cluster load (critical tasks like disaster recovery are prioritized).
  - Automatic retry with exponential backoff for failed tasks.
  - Dead-letter queue for tasks that fail after maximum retries, enabling manual intervention.
- **Deployment**: Containerized with Docker, deployable on Kubernetes with Helm charts for easy scaling.

##### Use Cases
- Distributed data backup and migration for object storage clusters.
- Batch processing of image metadata (resizing, format conversion, tagging).
- Consistency checks across distributed storage nodes.

#### 2. Distributed Cache System & Web Framework
**Duration**: Dec 2022 - Feb 2023  
**Role**: Independent Development (Personal Project)  
**Tech Stack**: Golang, Etcd, Protobuf, LRU, Consistency Hash, Gin  

##### Project Overview
A dual-purpose system combining a high-availability distributed cache and a lightweight web framework, designed to accelerate data access for distributed storage services. The cache system provides low-latency data access, while the web framework simplifies API development for storage operations.

##### Cache System Features
- **High Performance**:
  - Implemented LRU (Least Recently Used) eviction policy with configurable cache size.
  - Used read-write locks for concurrency control, with fine-grained locking to maximize throughput (100K+ QPS per node).
  - Supported cache expiration and automatic cleanup of stale keys.
- **Consistency & Reliability**:
  - Implemented SingleFlight mechanism to prevent cache breakdown (thundering herd problem).
  - Used Protobuf for efficient data serialization/deserialization between cache nodes.
  - Supported master-slave replication for data redundancy and fault tolerance.
- **Scalability**:
  - Applied consistency hash algorithm for uniform data distribution across nodes.
  - Supported horizontal scaling without data migration (new nodes automatically take over a portion of the hash ring).
- **Service Discovery & Fault Tolerance**:
  - Integrated Etcd for dynamic service registration and discovery.
  - Implemented health checks (heartbeat mechanism) between nodes to detect failures.
  - Designed fault recovery based on Raft-like term election, ensuring 99.9% cluster availability.

##### Web Framework Features
- **Dynamic Routing**: Supported prefix-based routing and route grouping for API versioning.
- **Middleware Support**: Built-in middleware for authentication, logging, rate limiting, and error recovery.
- **Context Management**: Unified context object for request/response tracking, parameter injection, and goroutine management.
- **Performance Optimization**: Context pool to reduce memory allocation overhead, improving API response time by 20%.

##### Use Cases
- Caching hot image metadata for object storage services.
- Accelerating frequently accessed storage configuration data.
- Building RESTful APIs for storage cluster management (node status, data usage, scaling).