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
  * Supervisor: Engineering Team Lead

* Mar 2023 - 2024: Backend Development Intern
  * Kuaishou, Beijing, China
  * Team: Cloud-Native Application - Basic Platform Department
  * Duties included:
    * Developed unified log monitoring SDK, integrating diverse logs, standardizing remote/local log reporting, and building end-to-end monitoring chain from source to sink
    * Designed pluggable architecture via plugin factory, enabling non-intrusive extension and supporting both local and remote configuration management
    * Implemented self-developed HTTP client with retry strategy, context injection, codec, and middleware hooks, enhancing SDK reliability
    * Integrated OpenTelemetry for distributed tracing, designing trace ID generation and exporter components to connect monitoring workflows
    * Optimized cloud-native platform performance by introducing multi-level caching and message queues, reducing database load by 40%
    * Built Elasticsearch indexes for deployment metrics and retrieval scripts, improving data query performance by 35%
    * Designed refined resource management workflows, saving ~25% of production environment resources via granular allocation
  * Supervisor: Engineering Team Lead

  

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

Additional Information
======
* Location: Beijing, China
* Email: trueno_cb@163.com
* GitHub: github.com/TruenoCB