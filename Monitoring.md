
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

Distribute tasks accross a set of resources. 
Distribute incoming application traffic across EC2 instances, containers, IP address and AWS Lambda functions.
Can work with EC2 auto-scaling. 
ELB components - rules, listeners and target groups

### Application Load Balancer

Specifically for HTTP and HTTPS traffic.
- Route traffic based on requested data - make routing decisions based on HTTP protocol
- Sends response directly to the client - can reply directly to client with some fixed response to reduce work on backend server.
- Uses TLS offloading 
- Secures traffic
- Use the round-robin routing algorithm - ensure the each server receives the same number of request in general.
- Use the least outstanding request routing algorithm - when a request is sent to the backend server and a response hasn't been received yet. When 2 EC2 instances have different size, CPU utilization will be different. 
- Use sticky sessions - use an HTTP cookie to remeber across connections which server to send the traffic to.

### Network Load Balancer

Support TCP, UDP and TLS protocols.
- use a flow hash routing algorithm
- has sticky sessions - sessions are based on source IP of client.
- support TLS offloading
- handles millions of requests per second.
- Support static and elastic IP addresses
- Preservers source IP address

[[EC2 Auto Scaling]]
