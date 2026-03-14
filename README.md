# GreenVision Cloud 🌿☁️
**Unified Multi-Cloud Carbon Management & Infrastructure Integration Platform**

## 📌 Project Overview
GreenVision Cloud is an enterprise-grade integration platform built to solve the "Carbon Visibility Challenge". It synchronizes data across **AWS, Azure, and GCP** to provide a unified observability layer for energy consumption, carbon emissions, and cost optimization.

> **Note:** This repository serves as a **Showcase**. The core implementation remains in a private repository to protect API integration logic and proprietary security protocols.

## ⚙️ System Integration & Architecture
This project focuses on the "connective tissue" between cloud providers and actionable business intelligence.

* **Multi-Cloud Data Ingestion:** Developed a robust pipeline that connects to **AWS CloudWatch Logs** and **Azure Monitor APIs** on configurable intervals to ingest raw system metrics.
* **Normalization Engine:** Processes raw bytes and compute minutes into kilowatt-hours (kWh) and subsequently into $kgCO_{2}$ using regional carbon intensity factors.
* **AI Integration:** Leverages **AWS Lex** for automated assistance and **TensorFlow.js/Random Forest** models to generate rightsizing recommendations based on ingested usage patterns.
* **Security & Compliance Integration:** Implemented **AES-256 encryption**, **JWT authentication**, and audit-ready reporting aligned with **MoEFCC (India)**, **EU Green Deal**, and **US EPA** standards.

## 🛠️ Tech Stack
* **Backend & Integration:** Node.js, Express, Cloud SDKs (AWS, Azure, GCP), Kubernetes.
* **Data Engineering:** MongoDB (Aggregation & Time-series storage), Agenda/Bull (Task Schedulers).
* **Frontend Observability:** React.js, Vite, Material UI, Socket.io for real-time telemetry.

## 📊 Key Features
* **Real-Time Carbon Tracking:** Live KPIs and sparklines for emission trends across all major providers.
* **Action Layer:** Rule-based AI recommendations for resource cleanup and offset strategy planning.
* **Immutable Audit Logs:** Hash-chained logs to ensure data integrity for government sustainability audits.
* **Automated Reporting:** Instant PDF/CSV exports for ESG disclosure and regulatory compliance.

## 📂 Project Assets & Documentation
Access the deep-dive technical resources for this project:

- **Architecture Deck:** [`docs/presentation/GreenVision-Deck.pdf`](./docs/presentation/GreenVision-Deck.pdf)
- **Project Overview:** [`docs/overview.pdf`](./docs/overview.pdf)
- **System Diagrams:** See `/diagrams` for Architecture, Data-Flow, and AI-Flow SVGs.
- **Visual Demos:** High-resolution screenshots and GIFs of the AI flow and dashboard are available in `/media`.

## 🛣️ Roadmap
- [ ] Scaling data schedulers with Redis for high-concurrency environments.
- [ ] Integrating **GCP** full-feature metrics (currently in progress).
- [ ] Infrastructure hardening using Secrets Manager and WAF integration.

## 🤝 Contact
**Shruti Deshmane**
- **Email:** [shrutideshmane93@gmail.com]
- **LinkedIn:** [https://www.linkedin.com/in/shruti-deshmane-ba7897358]
