# **Mid to Senior Backend Engineer (Java)**

## 1. **Core Java & Backend Fundamentals**

1. Explain how the **JVM manages memory**. What are the different memory areas (Heap, Stack, Metaspace)? How would you troubleshoot an `OutOfMemoryError`?
2. How does **concurrency** work in Java? Compare `synchronized`, `ReentrantLock`, and `Atomic` classes. When would you use one over the other?
3. What is the difference between `HashMap` and `ConcurrentHashMap`? How does `ConcurrentHashMap` achieve thread safety without locking the entire map?
4. Describe the **classloading mechanism** in Java. How can you implement a custom classloader?
5. What are the **performance implications** of using reflection in production systems?

------

## 2. **Spring Ecosystem**

1. How does **Spring Boot auto-configuration** work? How would you disable a specific auto-configuration?
2. Explain the difference between `@Controller` and `@RestController`. How do you handle **exception handling** globally in a Spring Boot application?
3. What is **Spring Security**’s filter chain? How would you implement **OAuth2** with JWT in a microservices architecture?
4. When would you use **Spring WebFlux** over Spring MVC? What are the trade-offs in terms of performance and complexity?
5. How do you manage **transactions** in Spring? What’s the difference between `REQUIRED` and `REQUIRES_NEW` propagation levels?

------

## 3. **Microservices & Architecture**

1. How do you ensure **data consistency** across microservices? Discuss patterns like Saga, CQRS, and Event Sourcing.
2. What’s your approach to **service discovery** and **load balancing** in a Kubernetes environment?
3. How would you design a **rate-limiting mechanism** for a REST API used by millions of clients?
4. Describe a **distributed transaction** scenario you’ve handled. What tools or patterns did you use?
5. How do you manage **API versioning** in a multi-service ecosystem? What are the pros and cons of URI vs header-based versioning?

------

## 4. **Messaging & Streaming (Kafka, RabbitMQ)**

1. How does **Kafka** guarantee **exactly-once semantics**? What trade-offs are involved?
2. Explain **consumer group rebalancing** in Kafka. How do you handle it gracefully?
3. When would you choose **RabbitMQ** over Kafka? Give a real-world example.
4. How do you handle **message reprocessing** or **dead-letter queues** in an event-driven system?
5. What’s the difference between **Kafka Streams** and a simple producer-consumer setup?

------

## 5. **Data & Storage (SQL, NoSQL, Redis)**

1. Design a **database schema** for a multi-tenant SaaS platform. How would you handle scaling and isolation?
2. How do you choose between **PostgreSQL** and **MongoDB** for a given use case?
3. What are **Redis use cases** beyond caching? How would you implement **rate limiting** using Redis?
4. How do you identify and fix **slow SQL queries**? What tools and techniques do you use?
5. Explain **indexing strategies** in PostgreSQL. How do `B-Tree`, `GIN`, and `BRIN` indexes differ?

------

## 6. **DevOps & CI/CD**

1. Walk me through a **CI/CD pipeline** you’ve built for a Java microservice. What stages did you include?
2. How do you manage **secrets and configuration** in a Kubernetes deployment?
3. What’s your approach to **containerizing a Spring Boot application** for production? How do you optimize image size?
4. How do you perform **blue-green deployments** or **canary releases** in Kubernetes?
5. How would you debug a **pod crash-loop** in production?

------

## 7. **API Design & Security**

1. How do you design a **RESTful API** that supports pagination, filtering, and sorting efficiently?
2. Explain **JWT structure** and how you’d implement **token refresh** securely.
3. How do you protect against **CSRF**, **XSS**, and **SQL injection** in a Java backend?
4. What’s your approach to **API documentation** and contract testing (e.g., OpenAPI, Spring REST Docs)?
5. How would you implement **idempotency** in a payment API?

------

## 8. **System Design & Scalability**

1. Design a **URL shortener** like [bit.ly](https://bit.ly/). Focus on scalability, caching, and database sharding.
2. How would you design a **real-time notification system** handling 1 million events per second?
3. What’s your approach to **caching strategy** (write-through, write-behind, cache-aside) in a distributed system?
4. How do you scale a **relational database** beyond a single node? Discuss sharding, replication, and partitioning.
5. How would you monitor and trace **distributed transactions** across microservices? (e.g., OpenTelemetry, Jaeger)

------

## 9. **Nice-to-Have / Advanced**

1. How does **reactive programming** differ from imperative programming? Give an example using Spring WebFlux.
2. What’s your experience with **GraphQL**? How does it compare to REST for complex frontend needs?
3. Explain **Event Sourcing** and **CQRS**. When are they beneficial, and what are the challenges?
4. How do you handle **high-load systems** with millions of requests/day? What bottlenecks did you encounter?
5. What **AI tools** do you use to improve development productivity? Give a concrete example.

------

## 10. **Behavioral & Ownership**

1. Tell me about a time you took **ownership** of a failing production system. What did you do, and what was the outcome?
2. Describe a **system design** you proposed that improved scalability or reliability. How did you convince your team?
3. How do you ensure **code quality and maintainability** across a team?
4. Give an example of a **technical debt** you decided to prioritize over new features. How did you justify it?
5. How do you stay updated with new technologies, and how do you decide when to adopt them?