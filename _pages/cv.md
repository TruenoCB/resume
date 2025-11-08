---
permalink: /cv/
title: "Curriculum Vitae"
author_profile: true
---

## Education
- **Master of Software Engineering**, Dalian University of Technology (DUT), Sep 2021 - Present
  - Relevant Coursework: Distributed Systems, Cloud Computing, Data Structure & Algorithms, Database Systems
- **Bachelor of E-Commerce**, Dalian Maritime University (DMU), Sep 2017 - Jun 2021
  - Graduation Thesis: "Design and Implementation of a Lightweight Distributed File Sharing System"
  - GPA: 3.6/4.0 (Top 10% of Major)

## Professional Experience
### Distributed Storage Engineer | JD.com (Jul 2022 - Present)
**Team**: Core Storage Platform Department  
**Reporting To**: Senior Engineering Manager  
**Key Responsibilities**: Design, develop, and optimize distributed object storage and image storage systems to support JD's global e-commerce infrastructure. Collaborate with cross-functional teams (product, operations, SRE) to deliver reliable, scalable, and cost-effective storage solutions.

#### Key Projects & Achievements:
1. **High-Throughput Image Storage Service**
   - Led the design and development of a dedicated image storage service for JD's product catalog (100M+ SKUs) and marketing campaigns.
   - Implemented tiered storage (SSD for hot data, HDD for cold data) and intelligent prefetching based on user access patterns, reducing storage costs by 15%.
   - Built a distributed upload/download acceleration layer with CDN integration, supporting 50,000+ peak QPS and 100M+ daily image transactions.
   - Designed fault-tolerant mechanisms (data replication across 3 zones) and disaster recovery processes, achieving 99.99% service availability.
   - Tech Stack: Golang, Gin, Redis Cluster, MinIO, Kafka, Docker, Kubernetes

2. **Object Storage Consistency & Performance Optimization**
   - Optimized the Raft-based metadata replication protocol for object storage, reducing consistency latency by 30% (150ms → 105ms) and improving write throughput by 25%.
   - Implemented incremental data synchronization between cross-region storage clusters, cutting inter-region bandwidth usage by 40%.
   - Developed a Redis-based distributed lock service to resolve concurrent write conflicts, reducing data error rates to near zero.
   - Tuned MySQL database for storage metadata (index optimization, query rewriting), reducing metadata query latency by 60% (80ms → 32ms).
   - Tech Stack: Golang, Raft Protocol, Redis, MySQL, Protobuf

3. **Cloud-Native Storage Migration**
   - Led the migration of legacy monolithic storage systems to cloud-native architecture, leveraging Kubernetes for container orchestration and Helm for package management.
   - Implemented horizontal pod autoscaling (HPA) based on CPU/memory usage and request throughput, reducing resource waste by 25% during off-peak hours.
   - Built end-to-end CI/CD pipelines using Jenkins and GitLab CI, automating build, test, and deployment processes, shortening release cycles from 2 hours to 15 minutes.
   - Developed custom Kubernetes operators for storage cluster management (scaling, upgrading, fault recovery), reducing manual operations by 80%.
   - Tech Stack: Kubernetes, Helm, Docker, Jenkins, GitLab CI, Infrastructure as Code

4. **Storage Monitoring & Observability System**
   - Designed and deployed a comprehensive monitoring system for 1000+ storage nodes, covering metrics (throughput, latency, error rate, disk health).
   - Integrated Prometheus for metrics collection and Grafana for visualization, building custom dashboards for real-time cluster monitoring.
   - Developed custom exporters for storage-specific metrics (object count, storage utilization, replication status) and set up multi-level alerts (P0-P3) via Slack/Email.
   - Implemented log aggregation with ELK Stack, enabling root cause analysis of performance bottlenecks and faults within 5 minutes.
   - Tech Stack: Prometheus, Grafana, ELK Stack, Shell Scripting, Golang

#### Technical Stack Summary:
- Programming: Golang (Proficient), Java (Familiar), SQL, Shell, Protobuf
- Storage: Object Storage (MinIO/S3), Distributed File Systems, Tiered Storage, Image Optimization
- Databases & Middleware: MySQL, Redis Cluster, Kafka, Etcd
- Distributed Systems: Raft/Paxos, Data Replication, Distributed Lock, Fault Tolerance
- Cloud-Native: Docker, Kubernetes, Helm, CI/CD, HPA
- Monitoring: Prometheus, Grafana, ELK Stack, Custom Exporters

## Project Experience
### 1. GoFlow Async Task Processing Framework (Mar 2023 - Jul 2023)
- **Role**: Architecture Design & Core Development (Personal Project)
- **Objective**: Develop a high-performance asynchronous task framework for distributed storage scenarios (data backup, migration, consistency checks).
- **Key Features & Achievements**:
  - Scalable two-tier architecture: flowsvr (task scheduling, queue management) and worker (task execution, result reporting).
  - Performance optimization: Tuned MySQL connection pool, implemented Redis caching for task metadata, reduced lock contention → 4x throughput improvement (500 QPS → 2000 QPS).
  - Distributed coordination: Replaced MySQL row locks with Redis distributed locks to resolve multi-machine competition, reducing CPU usage by 35%.
  - Dynamic task management: Supported task priority adjustment, retries, and dead-letter queues for failed tasks.
  - Deployment: Containerized with Docker, supporting horizontal scaling via Kubernetes.
- **Tech Stack**: Golang, MySQL, Redis, Protobuf, Docker, Kubernetes, Gin

### 2. Distributed Cache System & Web Framework (Dec 2022 - Feb 2023)
- **Role**: Independent Development (Personal Project)
- **Objective**: Build a high-availability distributed cache system integrated with a lightweight web framework for storage service APIs.
- **Key Features & Achievements**:
  - Cache Engine: Implemented LRU eviction policy with read-write locks for concurrency control, supporting 100K+ QPS per node.
  - Consistency & Scalability: Applied consistency hash algorithm for data distribution, enabling horizontal scaling without data migration.
  - Fault Tolerance: Built service discovery via Etcd and Raft-like leader election, ensuring 99.9% cache cluster availability.
  - Web Framework: Supported dynamic routing, middleware (authentication, logging, rate limiting), and context management for RESTful APIs.
  - Performance Optimization: Designed a context pool to reduce goroutine creation overhead, improving API response time by 20%.
- **Tech Stack**: Golang, Etcd, Protobuf, LRU, Consistency Hash, Gin, Sync Package

## Technical Skills
### Core Competencies
| Category                | Skills                                                                 |
|-------------------------|-----------------------------------------------------------------------|
| Programming Languages   | Golang (85%), Java (70%), SQL (80%), Shell (75%), Protobuf (80%)       |
| Storage Technologies    | Object Storage (MinIO/S3), Image Storage, Distributed File Systems, Tiered Storage |
| Distributed Systems     | Raft/Paxos, Data Replication, Distributed Lock, Fault Tolerance, Load Balancing |
| Databases & Middleware  | MySQL (Index Tuning), Redis Cluster, Kafka, Etcd                      |
| Cloud-Native & DevOps   | Docker, Kubernetes, Helm, CI/CD (Jenkins/GitLab CI), Infrastructure as Code |
| Monitoring & Observability | Prometheus, Grafana, ELK Stack, Custom Metrics Exporters             |
| Foundations             | TCP/IP, Concurrency Control, Data Structures & Algorithms, Performance Tuning |

### Soft Skills
- Strong problem-solving abilities with a data-driven approach to engineering challenges.
- Excellent teamwork and cross-functional collaboration (worked with product, SRE, and frontend teams).
- Proactive self-learner with a passion for emerging technologies (cloud-native, distributed systems).
- Clear communication skills, able to articulate technical concepts to both technical and non-technical stakeholders.
- Detail-oriented with a focus on code quality, test coverage, and system reliability.

## Additional Information
- Technical Blog: [trueno.cloud](https://www.trueno.cloud) (Posts on distributed systems, storage optimization, and Golang development)
- Open Source Contributions: Active contributor to MinIO community (bug fixes for object storage)
- Certifications: Kubernetes Certified Application Developer (CKAD) – In Progress
- Hobbies: Technical writing, open-source development, fitness (boxing, running)
