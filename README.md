# GreenVision Cloud 🌿☁️
**Unified Multi-Cloud Carbon Management & Infrastructure Integration Platform**

## 📌 Project Overview
[cite_start]GreenVision Cloud is an enterprise-grade integration platform built to solve the "Carbon Visibility Challenge" [cite: 7-8]. [cite_start]It synchronizes data across **AWS, Azure, and GCP** to provide a unified observability layer for energy consumption, carbon emissions, and cost optimization[cite: 1, 5, 191].

> **Note:** This repository serves as a **Showcase**. The core implementation remains in a private repository to protect API integration logic and proprietary security protocols.

## ⚙️ System Integration & Architecture
This project focuses on the "connective tissue" between cloud providers and actionable business intelligence.

* [cite_start]**Multi-Cloud Data Ingestion:** Developed a robust pipeline that connects to **AWS CloudWatch Logs** and **Azure Monitor APIs** on configurable intervals to ingest raw system metrics[cite: 69, 71, 199].
* [cite_start]**Normalization Engine:** Processes raw bytes and compute minutes into kilowatt-hours (kWh) and subsequently into $kgCO_{2}$ using regional carbon intensity factors[cite: 74, 161, 240].
* [cite_start]**AI Integration:** Leverages **AWS Lex** for automated assistance and **TensorFlow.js/Random Forest** models to generate rightsizing recommendations based on ingested usage patterns[cite: 201, 207].
* [cite_start]**Security & Compliance Integration:** Implemented **AES-256 encryption**, **JWT authentication**, and audit-ready reporting aligned with **MoEFCC (India)**, **EU Green Deal**, and **US EPA** standards[cite: 194, 219, 222, 229].

## 🛠️ Tech Stack
* [cite_start]**Backend & Integration:** Node.js, Express, Cloud SDKs (AWS, Azure, GCP), Kubernetes[cite: 3, 5, 191].
* [cite_start]**Data Engineering:** MongoDB (Aggregation & Time-series storage), Agenda/Bull (Task Schedulers)[cite: 75, 233].
* [cite_start]**Frontend Observability:** React.js, Vite, Material UI, Socket.io for real-time telemetry[cite: 3, 79, 206].

## 📊 Key Features
* [cite_start]**Real-Time Carbon Tracking:** Live KPIs and sparklines for emission trends across all major providers[cite: 4, 79].
* [cite_start]**Action Layer:** Rule-based AI recommendations for resource cleanup and offset strategy planning[cite: 65, 117].
* [cite_start]**Immutable Audit Logs:** Hash-chained logs to ensure data integrity for government sustainability audits[cite: 203, 229].
* [cite_start]**Automated Reporting:** Instant PDF/CSV exports for ESG disclosure and regulatory compliance[cite: 107, 248].

## 📂 Project Assets & Documentation
Access the deep-dive technical resources for this project:

- **Architecture Deck:** [`docs/presentation/GreenVision-Deck.pdf`](./docs/presentation/GreenVision-Deck.pdf)
- **Project Overview:** [`docs/overview.pdf`](./docs/overview.pdf)
- **System Diagrams:** See `/diagrams` for Architecture, Data-Flow, and AI-Flow SVGs.
- **Visual Demos:** High-resolution screenshots and GIFs of the AI flow and dashboard are available in `/media`.

## 🛣️ Roadmap
- [ ] Scaling data schedulers with Redis for high-concurrency environments.
- [ ] [cite_start]Integrating **GCP** full-feature metrics (currently in progress)[cite: 132].
- [ ] Infrastructure hardening using Secrets Manager and WAF integration.

## 🤝 Contact
**Shruti Deshmane**
- **Email:** [shrutideshmane93@gmail.com]
- **LinkedIn:** [https://www.linkedin.com/in/shruti-deshmane-ba7897358]
