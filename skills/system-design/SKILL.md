---
name: system-design
description: Master system architecture, database design, scalability patterns, and distributed systems. Use when designing large-scale systems, optimizing databases, or solving architectural challenges.
sasmp_version: "1.3.0"
bonded_agent: 01-frontend-ui-specialist
bond_type: PRIMARY_BOND
---

# System Design & Architecture

## Quick Start

System design requires understanding multiple layers and trade-offs:

```
User Request Flow:
┌─────────┐
│  Client │
└────┬────┘
     │
  ┌──▼──┐
  │ LB  │ (Load Balancer)
  └──┬──┘
     │
  ┌──▼──────────┐
  │ Web Servers │
  └──┬──────────┘
     │
  ┌──▼──────────┐
  │   Cache     │ (Redis)
  └──┬──────────┘
     │
  ┌──▼──────────┐
  │  Database   │
  └─────────────┘
```

## Fundamental Concepts

### Scalability
- **Vertical Scaling**: Upgrading hardware (limited)
- **Horizontal Scaling**: Adding more machines (preferred)
- **Database Sharding**: Partitioning data across servers
- **Read Replicas**: Scaling read capacity

### Availability & Reliability
- **Redundancy**: Multiple instances, failover
- **Consistency**: Data accuracy across replicas (CAP theorem)
- **Fault Tolerance**: System survives component failures
- **Monitoring**: Detecting and alerting on issues

### Latency & Throughput
- **Latency**: Time to complete request (milliseconds)
- **Throughput**: Requests per second (RPS)
- **Response Time SLAs**: Defined performance targets
- **Caching**: Reducing latency with cached responses

## Database Design

### Relational Databases

#### Schema Design
- **Normalization**: Reducing redundancy (1NF, 2NF, 3NF)
- **Primary Keys**: Unique row identification
- **Foreign Keys**: Referential integrity
- **Indexing**: B-tree indexes for query optimization

#### Query Optimization
```sql
-- Indexed query for efficiency
SELECT u.id, u.name, COUNT(o.id) as order_count
FROM users u
LEFT JOIN orders o ON u.id = o.user_id
WHERE u.created_at > NOW() - INTERVAL '30 days'
GROUP BY u.id
ORDER BY order_count DESC
LIMIT 10;
```

#### Advanced Concepts
- **Transactions**: ACID properties
- **Isolation Levels**: Balancing consistency and performance
- **Sharding**: Horizontal partitioning
- **Replication**: Master-slave, multi-master

### NoSQL Databases

#### Document Databases (MongoDB)
- **Schema Flexibility**: Dynamic documents
- **Embedding**: Storing related data together
- **Indexing**: Similar to SQL databases
- **Aggregation**: Complex data transformations

#### Key-Value Stores (Redis)
- **In-Memory**: Ultra-fast access
- **Data Structures**: Strings, lists, sets, hashes, sorted sets
- **TTL**: Automatic expiration
- **Pub/Sub**: Message broadcasting

#### Wide-Column Stores (Cassandra)
- **Distributed**: Masterless architecture
- **Partitioning**: Data distribution across nodes
- **Consistency**: Tunable consistency levels
- **Time-Series**: Optimized for time-series data

## Caching Strategies

### Cache Types
1. **Cache-Aside Pattern**
   ```
   1. Check cache for data
   2. If miss, fetch from DB
   3. Update cache
   4. Return to client
   ```

2. **Write-Through Pattern**
   ```
   1. Write to cache
   2. Write to DB
   3. Return when both complete
   ```

3. **Write-Behind Pattern**
   ```
   1. Write to cache
   2. Return immediately
   3. Async write to DB
   ```

### Cache Invalidation
- **TTL**: Time-based expiration
- **Event-Driven**: Invalidate on data change
- **LRU**: Remove least recently used entries
- **Manual**: Explicit invalidation

## Microservices Architecture

### Service Boundaries
- **Domain-Driven Design**: Services around business domains
- **Single Responsibility**: Each service has one reason to change
- **Independent Deployment**: Separate CI/CD pipelines
- **Technology Diversity**: Different stacks per service

### Communication Patterns
- **Synchronous**: REST, gRPC for request-response
- **Asynchronous**: Message queues for loose coupling
- **Event-Driven**: Publishing domain events
- **Service Mesh**: Istio, Linkerd for advanced routing

### Data Management
```
Monolith:          Microservices:
┌─────────┐        ┌─────────┐   ┌─────────┐
│ Service │        │Service 1│   │Service 2│
└─────────┘        └────┬────┘   └────┬────┘
    │                   │             │
┌───▼────────────────┐  │             │
│   Single Database   │  │             │
└────────────────────┘  │             │
                        │             │
                    ┌───▼──────┐  ┌───▼──────┐
                    │ Database1 │  │ Database2 │
                    └───────────┘  └───────────┘
```

### Event-Driven Design
- **Event Sourcing**: Store state as immutable events
- **CQRS**: Separate read and write models
- **Saga Pattern**: Distributed transactions
- **Idempotency**: Safe retry operations

## Load Balancing

### Algorithms
- **Round Robin**: Sequential distribution
- **Least Connections**: Forward to least busy server
- **IP Hash**: Route based on client IP (sticky sessions)
- **Weighted**: Distribute based on server capacity

### Load Balancer Types
- **Application LB**: Layer 7 (HTTP/HTTPS)
- **Network LB**: Layer 4 (TCP/UDP)
- **Global LB**: Geographic distribution
- **DNS LB**: Route resolution

## Monitoring & Observability

### Metrics
- **System Metrics**: CPU, memory, disk, network
- **Application Metrics**: Request rate, error rate, latency
- **Business Metrics**: User activity, conversions
- **Custom Metrics**: Application-specific data

### Logging
- **Structured Logging**: JSON format for parsing
- **Log Levels**: DEBUG, INFO, WARN, ERROR, CRITICAL
- **Correlation IDs**: Tracking requests across services
- **Centralized Logging**: ELK, Splunk for aggregation

### Tracing
- **Distributed Tracing**: Following requests across services
- **Span Analysis**: Understanding service interactions
- **Bottleneck Identification**: Finding performance issues
- **Tools**: Jaeger, Zipkin, DataDog APM

## Best Practices

1. **Design for Failure**: Assume components will fail
2. **Monitoring First**: Implement observability upfront
3. **Incremental Scaling**: Start simple, scale when needed
4. **Document Trade-offs**: Explain architectural decisions
5. **Security**: Defense in depth, principle of least privilege
6. **Testing**: Load testing, chaos engineering
7. **Automation**: Infrastructure as code, CI/CD

## Learning Resources

- System Design Roadmap: https://roadmap.sh/system-design
- Designing Data-Intensive Applications: https://dataintensive.fun
- AWS Architecture Center: https://aws.amazon.com/architecture
- Microservices.io: https://microservices.io
