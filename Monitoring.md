
# Amazon CloudWatch

You can use CloudWatch to:

-   Detect anomalous behavior in your environments
-   Set alarms to alert you when something is not right
-   Visualize logs and metrics with the AWS Management Console
-   Take automated actions like scaling
-   Troubleshoot issues
-   Discover insights to keep your applications healthy

CloudWatch is a managed service that you can use for monitoring without managing the underlying infrastructure.

You can get started with custom metrics by programmatically sending the metric to CloudWatch using the PutMetricData API.

You can use external or custom tools to ingest and analyze CloudWatch metrics using the GetMetricData API.

CloudWatch metric, alarm, dashboard, logs
log event -> log stream -> log groups

Alarm has 3 states:
-   **OK:** The metric is within the defined threshold. Everything appears to be operating like normal.
-   **ALARM:** The metric is outside the defined threshold. This could be an operational issue.
-   **INSUFFICIENT_DATA:** The alarm has just started, the metric is not available, or not enough data is available for the metric to determine the alarm state.

## Amazon Elastic Load Balancing


