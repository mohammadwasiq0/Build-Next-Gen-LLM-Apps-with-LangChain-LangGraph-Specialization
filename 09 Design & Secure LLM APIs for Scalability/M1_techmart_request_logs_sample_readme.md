# TechMart Request Logs Dataset

## Overview
This dataset contains anonymized API request logs from TechMart's monolithic e-commerce platform. The data supports microservices decomposition analysis by revealing request patterns, database contention, and service dependencies.

## Dataset Schema
- `request_id`: Unique identifier for each request (e.g., "req_001")
- `timestamp`: Request timestamp in ISO 8601 format
- `endpoint`: API endpoint path
- `method`: HTTP method (GET, POST, etc.)
- `response_time_ms`: Total response time in milliseconds
- `status_code`: HTTP status code
- `service`: Service domain (user-service, product-service, recommendation-service)
- `database_queries`: Number of database queries executed
- `db_time_ms`: Total database query time in milliseconds
- `external_calls`: List of services called (for recommendation-service)

## Usage Notes
- Load using `profile_monolith()` utility in the starter notebook
- Analyze request patterns to identify service boundaries
- Use database query metrics to identify contention bottlenecks
- Ensure compliance with TechMart data handling policies when storing derived metrics

## Sample Size
The full dataset contains 10,000 requests. This sample file includes 10 representative examples. The complete dataset will be provided in the Coursera lab environment.

## Key Patterns
- `/api/users/*` endpoints: User management domain
- `/api/products/*` endpoints: Product catalog domain
- `/api/recommendations`: Recommendation domain (depends on user and product services)
- Database contention visible in high `db_time_ms` values

## Privacy & Compliance
All customer identifiers have been anonymized. Request payloads are excluded. Follow TechMart's data handling checklist when exporting metrics or sharing results.

