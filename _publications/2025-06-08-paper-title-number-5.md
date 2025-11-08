---
permalink: /projects/
title: "Project Experience"
author_profile: true
---

## Key Projects

### 1. GoFlow Async Task Processing Framework
**Duration**: Mar 2023 - Jul 2023  
**Role**: Architecture Design & Core Development (Personal Project)  
**Tech Stack**: Golang, MySQL, Redis, Protobuf, Docker, Kubernetes, Gin  

#### Project Overview
A high-performance asynchronous task processing framework designed specifically for distributed storage scenarios (e.g., data backup, migration, consistency checks, and batch processing). The framework enables developers to build scalable, fault-tolerant task workflows with minimal code.

#### Core Features
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

#### Use Cases
- Distributed data backup and migration for object storage clusters.
- Batch processing of image metadata (resizing, format conversion, tagging).
- Consistency checks across distributed storage nodes.

### 2. Distributed Cache System & Web Framework
**Duration**: Dec 2022 - Feb 2023  
**Role**: Independent Development (Personal Project)  
**Tech Stack**: Golang, Etcd, Protobuf, LRU, Consistency Hash, Gin  

#### Project Overview
A dual-purpose system combining a high-availability distributed cache and a lightweight web framework, designed to accelerate data access for distributed storage services. The cache system provides low-latency data access, while the web framework simplifies API development for storage operations.

#### Cache System Features
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

#### Web Framework Features
- **Dynamic Routing**: Supported prefix-based routing and route grouping for API versioning.
- **Middleware Support**: Built-in middleware for authentication, logging, rate limiting, and error recovery.
- **Context Management**: Unified context object for request/response tracking, parameter injection, and goroutine management.
- **Performance Optimization**: Context pool to reduce memory allocation overhead, improving API response time by 20%.

#### Use Cases
- Caching hot image metadata for object storage services.
- Accelerating frequently accessed storage configuration data.
- Building RESTful APIs for storage cluster management (node status, data usage, scaling).
