# Bazaar-Case-Study
Bazaar Case Study - An intelligent, scalable stock management solution for managing inventory across thousands of retail stores. The system leverages modern backend technologies and AI to ensure real-time accuracy, performance, and fault tolerance.

#### About the Project
This system was designed to streamline stock tracking in large retail networks by combining:
- **Event-driven architecture** (Kafka) for near real-time updates
- **AI-enhanced inventory logic** for threshold detection and forecasting
- **Redis caching** for ultra-fast reads
- **MySQL** with read/write separation for scalability
- **Audit logging** for full traceability

#### Evolution Overview

##### Phase 1: Monolithic MVP
- Stock update and retrieval via single DB
- No async or caching layers

##### Phase 2: Performance Boost
- Redis for caching frequent reads
- Async background tasks to reduce response time

##### Phase 3: Scalable System
- Kafka for async communication
- AI logic to flag low inventory and predict demand
- Read/Write DB separation
- Rate limiting and auditing enabled

#### Core Tech Stack
- **FastAPI** for async REST APIs
- **Kafka** for event processing
- **Redis** for fast data access
- **MySQL** with replica support
- **AI/Rules Engine** for stock intelligence

#### Key API Endpoints
| Method | Route | Description |
|--------|-------|-------------|
| POST | `/update-stock/{store_id}/{product_id}` | Update stock and fire Kafka event |
| GET | `/get-stock/{store_id}/{product_id}` | Get stock (cache → DB fallback) |
| GET | `/audit-logs` | View change history |

#### AI & Automation
- Notifies when stock is below **dynamic thresholds**
- Predicts demand trends to support timely restocking
- Triggers intelligent alerts with minimal human input

#### Real-World Impact
- Prevents **stock shortages** and overstock scenarios
- Keeps stock data **synchronized across all branches**
- Supports massive scaling with **low latency** and **resilience**

#### Features Summary
- Event-driven & async by design
- Caching with Redis
- AI-based stock thresholding
- Read/write DB optimization
- Rate limiting & full audit trail

