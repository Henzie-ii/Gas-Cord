# Gas-Cord-Platform

GasCord is a multi-sided e-commerce and asset-tracking ecosystem designed for cooking gas retail and logistics. The platform streamlines consumer product catalog browsing and refill swapping while ensuring strict backend tracking of high-value physical cylinders using automated database ledger records.

System Architecture Overview

This project is built using a hybrid service architecture within a single monorepo:

*   **`cloudgas-backend-django/`**: High-security core service. Utilizes Django's built-in Admin panel and ORM engine to manage inventory master catalogs, user profiles, system security controls, and structural database migrations.
*   **`cloudgas-api-fastapi/`**: Asynchronous processing engine. Handles real-time operational workloads, customer mobile checkouts, and high-velocity driver cylinder scanning tracking logs.
*   **`cloudgas-frontend-react/`**: Mobile-first responsive user interface shared dynamically across customer screens and the driver field portal.
*   **Database**: A shared PostgreSQL instance acting as the unified source of truth for both backend services.

---

## 📂 Repository Layout

```text
gas-cord-platform/
├── backend-django/     # Administrative panel & core database models
├── api-services-fastapi/        # Real-time high-speed API endpoints
├── frontend-react/     # Unified mobile-responsive frontend views
└── docker-compose.yml           # Local database and infrastructure service config

