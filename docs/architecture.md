# System Architecture: GreenVision Cloud

## High-Level Design
GreenVision Cloud is designed as a modular, event-driven integration platform. It utilizes a decoupled architecture to manage high-frequency data ingestion from multiple cloud providers while maintaining a responsive user interface.

![System Architecture](./diagrams/GreenVision_Cloud-System_Architecture.drawio.png)

### Component Breakdown
* **Frontend:** Built with **React 18 and Vite**, utilizing **MUI** for the dashboard interface. It consumes real-time telemetry via **Socket.io** and standard state management through **React Query**.
* **API Layer:** An **Express 5** gateway managing routing, JWT-based authentication, and request dispatching.
* **Services Layer:** The core "Integration" hub containing Cloud SDKs, Rule Engines, and Schedulers.
* **Persistence Layer:** **MongoDB** (via Mongoose) stores time-series cloud metrics, carbon footprints, and audit logs.
* **Real-time & Background Jobs:** **Socket.io** for live event broadcasting and **Agenda/Bull** for scheduling recurring metric ingestion tasks.

## System Workflow & Data Flow
The following sequence describes the interaction between the client, API, and the audit-chain middleware:

![Data Flow Sequence](./diagrams/GreenVision_Cloud-Data_flow.drawio.png)

1. **Request Lifecycle:** A client request (authenticated via JWT) enters through the API Gateway. The Controller dispatches the request to the relevant Service.
2. **Audit Middleware:** Every state-changing operation passes through an audit middleware that generates a **hash-chained log entry**.
3. **Real-time Updates:** As background schedulers pull new data, the Socket.io server pushes live updates to the browser.

## AI Recommendation Logic
The platform utilizes a **Rule-Based Engine** to transform raw infrastructure data into actionable insights:

![AI Recommendation Flow](./diagrams/GreenVision_Cloud-AI_Recommendation_Flow.drawio.png)

* **Inputs:** Ingests `CloudMetrics` (CPU, network, storage) and `CloudLogs` (AWS CW, Azure Logs, GCP Logs).
* **Processing:** Evaluates data against pre-set thresholds and heuristics to generate recommendations for rightsizing and cleanup.
* **Delivery:** Notifications are pushed via WebSocket and emailed via Nodemailer.

## Security & Integrity: Hash-Chained Audit Logs
To meet strict government compliance (MoEFCC/GDPR), the system implements a tamper-evident audit chain:

![Audit Chain Immutability](./diagrams/GreenVision_Cloud-Audit_Chain_immutability.drawio.png)

* **Immutability:** Each log entry contains its own hash and the hash of the previous entry (`prevHash`).
* **Verification:** If any historical log entry is altered, the hash chain breaks, and verification fails, ensuring a fully auditable compliance trail.

## Tech Stack Summary
* **Backend:** Node.js, Express, Mongoose, Socket.io, Agenda/Bull.
* **Frontend:** React 18, Vite, Material UI, React Router, Chart.js.
* **Integrations:** AWS SDK v3, Azure SDK, Google Cloud Client, Kubernetes Client.
