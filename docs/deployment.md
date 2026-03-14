# Deployment Architecture

This document outlines the conceptual deployment model for GreenVision Cloud services and their dependencies.

## Service Infrastructure
* **Frontend:** The React and Vite application is designed to be served via static hosting or a Content Delivery Network (CDN).
* **Backend API:** A Node.js and Express service that handles the core integration logic and API gateway functions.
* **Database:** A MongoDB cluster used for persistence of metrics, user data, and audit chains.
* **Real-time and Schedulers:** Socket.io handles live updates on the API host, while Agenda/Bull workers manage background metric ingestion and notification queues.

## Environment Dependencies
* **Connectivity:** A valid MongoDB connection string and SMTP provider settings for email notifications.
* **Integration Credentials:** Cloud provider credentials (AWS, Azure, GCP) configured with least-privilege roles.
* **Encryption Secrets:** A secure JWT secret for token signing and verification.

## Runtime and Scaling
* **Security Configuration:** CORS must be configured for the specific frontend origin, with HTTPS termination managed at the ingress or load balancer level.
* **Health Monitoring:** Continuous health checks are required for both the API service and the background workers.
* **Scaling Strategy:** The architecture supports horizontal scaling for the API and workers. Horizontal scaling of the Socket.io and job queue services requires the addition of a Redis adapter.
