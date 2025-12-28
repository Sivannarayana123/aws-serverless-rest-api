# aws-serverless-rest-api
Serverless REST API built on AWS using API Gateway, Lambda, and DynamoDB


**Project Overview:**
- This project demonstrates the design and implementation of a serverless REST API architecture on Amazon Web Services (AWS).
- The goal of this project is to understand how backend APIs can be built and scaled without managing servers, using fully managed AWS services.
- The architecture follows event-driven and serverless principles, focusing on scalability, cost optimization, and security.

**Architecture Overview:**
**Traffic Flow :**
1. Client sends an HTTP request to the API endpoint
2. Request reaches Amazon API Gateway
3. API Gateway triggers an AWS Lambda function
4. Lambda processes the request logic
5. Data is read from or written to Amazon DynamoDB
6. Response is returned back to the client via API Gateway


**AWS Services Used:**

- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- IAM Roles & Policies
- Amazon CloudWatch


**Step-by-Step Implementation:**

**Step 1: Create DynamoDB Table**
- Created a DynamoDB table to store application data.
- Defined partition key for efficient data access.
- Enabled on-demand capacity for automatic scaling.

   **Purpose:**
   Provides a fully managed, scalable NoSQL database.

**Step 2: Create IAM Role for Lambda**

- Created an IAM role with permissions to access DynamoDB and CloudWatch.
- Attached least-privilege policies.

  **Security Principle:**
  Avoid hard-coded credentials and use IAM roles.

**Step 3: Create AWS Lambda Function**

- Created a Lambda function to handle API requests.
- Implemented basic logic to read/write data to DynamoDB.
- Configured execution role using IAM.

  **Why Lambda? :**
  Automatically scales and runs code without managing servers.

**Step 4: Configure API Gateway**

- Created a REST API using Amazon API Gateway.
- Defined HTTP methods (GET / POST).
- Integrated API Gateway with Lambda function.

  **Purpose:**
  Acts as the front door for client requests.

**Step 5: Enable Logging & Monitoring**

- Enabled CloudWatch logs for Lambda execution.
- Monitored API requests, errors, and execution time.

**Security Best Practices Implemented:**

1. IAM roles instead of access keys
2. Least privilege permissions for Lambda
3. No public database access
4. CloudWatch logging enabled

**Key Learnings:**

- Understanding serverless architecture concepts
- Building APIs without managing infrastructure
- Event-driven request handling
- IAM role-based security
- Monitoring serverless workloads

**Notes:**

- This project was implemented as a hands-on learning exercise.
- No sensitive credentials or account information are stored in this repository.
