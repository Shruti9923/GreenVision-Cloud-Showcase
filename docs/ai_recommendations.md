# AI Recommendations (Rule-Based Engine)

The GreenVision Cloud optimization engine uses a deterministic, rule-based approach to provide explainable and actionable advice for cloud infrastructure.

## Inputs and Data Sources
* **Cloud Metrics:** Real-time data including CPU utilization, network IO, instance types, and storage usage.
* **System Logs:** Analysis of provider logs to identify errors, patterns, or anomalies.
* **Configuration Thresholds:** Pre-defined hygiene rules regarding idle resources and utilization benchmarks.

## Optimization Logic
* **Compute Optimization:** Identifies underutilized instances and recommends downsizing to appropriate tiers with estimated cost savings.
* **Resource Cleanup:** Detects idle storage volumes, unattached assets, or orphaned snapshots and suggests immediate cleanup.
* **Infrastructure Rightsizing:** Analyzes low network and storage activity to suggest decommissioning or scaling down resources.
* **Governance Hygiene:** Recommends the enforcement of budget alerts, anomaly notifications, and resource tagging policies.

## Output and Delivery
* **Recommendation Cards:** Each insight includes the recommendation type, priority, potential savings, and a description.
* **Multi-Channel Delivery:** Insights are served via the dashboard API, triggered email summaries, and optional real-time pushes.
* **Baseline Fallback:** If telemetry data is sparse, the system provides generalized best-practice tips based on industry standards.
