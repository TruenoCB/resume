---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* M.S. in Software Engineering, Dalian University of Technology (DUT), 2024 (expected)
* B.S. in E-Commerce, Dalian Maritime University (DMU), 2021

Work experience
======
* Jun 2024 - Present: Distributed Storage Engineer
  * JD.com, Beijing, China
  * Team: Core Storage Platform Department
  * Duties included:
    * Designed and developed high-throughput image storage service supporting 100M+ daily uploads/downloads with 99.99% availability
    * Optimized Raft-based object storage metadata consistency, reducing replication latency by 30% and cross-region bandwidth consumption by 40%
    * Implemented Redis Cluster-based distributed cache layer for hot image data, improving access performance by 400% and reducing origin server load by 60%
    * Led cloud-native migration of legacy storage systems using Kubernetes, cutting off-peak resource waste by 25%
    * Built end-to-end monitoring system with Prometheus/Grafana, reducing mean time to resolve (MTTR) by 50%
    * Designed tiered storage strategy (SSD/HDD) and intelligent prefetching, lowering overall storage costs by 15%
  * Supervisor: Senior Engineering Manager

Skills
======
* Programming Languages
  * Golang (Proficient, 2+ years)
  * Java (Familiar, 3+ years)
  * SQL/NoSQL, Shell Scripting, Protobuf
* Storage Technologies
  * Object Storage (MinIO/S3-compatible)
  * Image Storage Optimization
  * Distributed File Systems, Tiered Storage (SSD/HDD)
* Distributed Systems
  * Raft/Paxos Consistency Protocols
  * Data Replication, Fault Tolerance
  * Distributed Lock, Load Balancing
* Databases & Middleware
  * MySQL (Index Tuning, Query Optimization)
  * Redis Cluster (Distributed Lock, Persistence)
  * Kafka, Etcd
* Cloud-Native & DevOps
  * Docker, Kubernetes, Helm
  * CI/CD (Jenkins, GitLab CI)
  * Infrastructure as Code
* Monitoring & Observability
  * Prometheus, Grafana
  * ELK Stack, Custom Metrics Exporters
* Foundations
  * TCP/IP Protocol, Concurrency Control
  * Data Structures & Algorithms
  * Performance Tuning

Projects
======
* Mar 2023 - Jul 2023: GoFlow Async Task Processing Framework (Personal Project)
  * Role: Architecture Design & Core Development
  * Key achievements:
    * Designed scalable two-tier architecture (flowsvr + worker) supporting horizontal scaling to 100+ nodes
    * Optimized throughput from 500 QPS to 2000 QPS via MySQL connection pool tuning and Redis caching
    * Resolved multi-machine competition with Redis distributed locks, reducing CPU usage by 35%
    * Implemented dynamic task priority adjustment based on storage cluster load

* Dec 2022 - Feb 2023: Distributed Cache System & Web Framework (Personal Project)
  * Role: Independent Development
  * Key achievements:
    * Built LRU cache with read-write locks, supporting 100K+ QPS per node
    * Applied consistency hash algorithm for seamless horizontal scaling
    * Integrated Etcd for service discovery and Raft-like fault tolerance (99.9% availability)
    * Developed lightweight web framework with dynamic routing and middleware support

Additional Information
======
* Technical Blog: trueno.cloud (Posts on distributed systems & storage optimization)
* Open Source: Active contributor to MinIO community (object storage bug fixes)
* Certifications: Kubernetes Certified Application Developer (CKAD) - In Progress
* Location: Beijing, China
* Email: trueno_cb@163.com
* GitHub: github.com/TruenoCB