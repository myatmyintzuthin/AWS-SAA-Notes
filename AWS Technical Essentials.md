Cloud computing is an on-demand delivery of IT resources over the internet with primarily pay-as-you-go pricing. AWS maintain infrustures, virtual data center and services.

## Six advantages of cloud computing

### Pay as you go

Instead of investing in data centers and hardwares, you only pay for the computing resources you use. 

### Benefit from massive economies of scale

As thousands of customers are aggregated in the cloud, lower pay as-you-go price.

### Stop guessing capacity

You can scale up and down as you want with a few minutes.

### Increase speed and agility

Resources are available to developers from weeks to minutes. Since cost and time it takes to experiment and develop is significantly lower.

### Realize cost savings

Cloud computing lets you focus on customers rather than on heavy lifting. 

### Go global in minutes

Applications can be deployed in multiple regions around the world with a few clicks. This means that you cn provide lower latency and a better experience for your customers at a minimal cost.


## 4 main aspects to consider while choosing right AWS region

- Latency
- Pricing
- Service availability
- Data compliance

## Availability Zones

![[images/Screenshot from 2023-02-23 10-10-24.png]]

Recommendation : Use at least 2 AZs, if one AZ fails, the application will have infrasture up and running in a second AZ to take over the traffic.

## Interacting with AWS

- AWS managment console
- AWS command line interface (CLI)
- AWS Software Development Kit (SDK)

## Security and AWS Shared Responsibilty Model

![[images/Screenshot from 2023-02-23 10-35-17.png]]

- Root user - use Multi-factor authentication

## IAM policies

```
{  
"Version": "2012-10-17",  
"Statement": [{  
"Effect": "Allow",  
"Action": "*",  
"Resource": "*"  
}]  
}
```

- version - define version of poilcy langauge. 
- effect - specifies whether the statement will allow or deny access. 
- action - describes the type of action should be allowed or denied.
- resource - specifies the object or objects that the policy statement covers.

## Role-based Access in AWS

![[images/Screenshot from 2023-02-27 09-45-00.png]]
# Other Topics

- [[Compute as a Service]]
- [[Networking]]
- [[Storage Types]]
- [[Databases]]
- [[Monitoring]]
- 