---
name: backend-systems
description: Master backend development including REST/GraphQL APIs, databases, authentication, caching, and microservices. Use when designing server architectures, building APIs, or optimizing database performance.
sasmp_version: "1.3.0"
bonded_agent: 01-frontend-ui-specialist
bond_type: PRIMARY_BOND
---

# Backend Systems

## Quick Start

Building a scalable backend requires understanding multiple layers:

```javascript
// Express.js REST API Example
const express = require('express');
const app = express();

app.use(express.json());

// User endpoint
app.get('/api/users/:id', async (req, res) => {
  try {
    const user = await db.user.findById(req.params.id);
    res.json(user);
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});

app.post('/api/users', async (req, res) => {
  const user = await db.user.create(req.body);
  res.status(201).json(user);
});
```

## Core Backend Concepts

### HTTP & Web Fundamentals
- **HTTP Methods**: GET, POST, PUT, DELETE, PATCH
- **Status Codes**: 2xx (success), 3xx (redirect), 4xx (client error), 5xx (server error)
- **Headers**: Content-Type, Authorization, CORS
- **REST Principles**: Resource-based URLs, stateless communication

### API Design

#### REST APIs
- **Resource Modeling**: Nouns for endpoints, verbs in HTTP methods
- **Versioning**: URL versioning, header versioning
- **Pagination**: Offset/limit, cursor-based pagination
- **Filtering & Sorting**: Query parameters for data manipulation
- **Error Handling**: Consistent error responses with proper codes

#### GraphQL
- **Schema Definition**: Types, queries, mutations, subscriptions
- **Resolvers**: Data fetching logic for each field
- **Performance**: Query optimization, DataLoader pattern
- **Subscriptions**: Real-time data updates via WebSockets

### Database Design

#### SQL (PostgreSQL, MySQL)
- **Normalization**: Normal forms, reducing redundancy
- **Indexing**: B-tree indexes, composite indexes, query planning
- **Transactions**: ACID properties, isolation levels
- **Optimization**: Query analysis, execution plans

#### NoSQL (MongoDB, Cassandra)
- **Document Design**: Schema flexibility, embedding vs. references
- **Sharding**: Horizontal scaling, shard key selection
- **Consistency**: Eventual consistency models
- **Replication**: Data redundancy and failover

### Authentication & Security

#### JWT (JSON Web Tokens)
```javascript
const token = jwt.sign(
  { userId: user.id, role: user.role },
  process.env.JWT_SECRET,
  { expiresIn: '24h' }
);
```

#### OAuth 2.0
- **Authorization Code Flow**: Third-party authentication
- **Scopes**: Permission levels for API access
- **Tokens**: Access tokens, refresh tokens

#### Security Practices
- **Password Hashing**: bcrypt, PBKDF2, Argon2
- **Rate Limiting**: Prevent brute force attacks
- **Input Validation**: Sanitize and validate all inputs
- **HTTPS**: Encryption in transit

### Caching Strategies

#### Redis Patterns
- **Cache-Aside**: Check cache, fetch from DB if miss
- **Write-Through**: Write to cache and DB simultaneously
- **Write-Behind**: Write to cache, async DB update
- **Cache Invalidation**: TTL, event-driven invalidation

### Microservices Architecture

#### Service Communication
- **Synchronous**: REST, gRPC for direct communication
- **Asynchronous**: Message queues (RabbitMQ, Kafka)
- **Service Discovery**: Finding service locations dynamically
- **Load Balancing**: Distributing requests

#### Data Management
- **Database per Service**: Data isolation and autonomy
- **Distributed Transactions**: Saga pattern for multi-service operations
- **Event Sourcing**: Event-based state management
- **CQRS**: Separate read and write models

## Best Practices

1. **API Design**: Clear, consistent endpoints with proper HTTP semantics
2. **Error Handling**: Meaningful error messages with appropriate status codes
3. **Logging**: Structured logging with request tracing
4. **Monitoring**: APM tools for performance tracking
5. **Testing**: Unit tests, integration tests, contract tests
6. **Documentation**: OpenAPI/Swagger for API contracts
7. **Versioning**: Backward compatibility or clear migration paths

## Common Patterns

- **Repository Pattern**: Abstract data access layer
- **Dependency Injection**: Loose coupling, easier testing
- **Middleware**: Cross-cutting concerns (logging, auth, CORS)
- **Circuit Breaker**: Fault tolerance for external service calls
- **Retry Logic**: Exponential backoff for transient failures

## Learning Resources

- Backend Roadmap: https://roadmap.sh/backend
- REST Best Practices: https://restfulapi.net
- GraphQL: https://graphql.org
- Design Patterns: https://refactoring.guru/design-patterns
