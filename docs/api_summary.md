# API Summary

The GreenVision Cloud API is a RESTful service that returns structured JSON. All successful responses follow the format `{ "success": true, "data": {...}, "message": "..." }`, while errors return `{ "success": false, "error": "...", "message": "..." }`.

##  Authentication
* **User Management:** Endpoints for signup, login, and profile management.
* **Security:** Implements token-based authentication for all protected infrastructure and compliance routes.

##  Cloud Metrics & Tracking
* **Inventory:** Fetch comprehensive lists of instances and services across AWS, Azure, and GCP.
* **Sustainability:** Access carbon footprint summaries, historical trends, and regional intensity data.
* **Kubernetes:** Retrieve workload and cluster-level summaries for containerized environments.

##  AI & Analytics
* **Optimization:** Access rule-based recommendations for resource rightsizing and cleanup.
* **Forecasting:** Retrieve cost and usage predictions based on historical patterns.
* **Anomaly Insights:** Fetch detailed logs and metrics regarding detected system anomalies.

##  Compliance & Audit
* **Audit Logs:** List and create entries for the system audit trail.
* **Chain Verification:** Verify the cryptographic integrity of individual logs or the complete hash chain.
* **Exporting:** Generate and download audit logs in CSV or PDF formats for external regulatory submission.

##  Notifications
* **Alerting:** Trigger on-demand email summaries of AI recommendations.
* **System Events:** Management endpoints for urgent system alerts and user notification preferences.
