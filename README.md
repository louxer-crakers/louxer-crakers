# Hi there, I'm Feriadi Putra 👋
### ☁️ Cloud & DevOps Engineer | AWS Architecture Enthusiast

I am a passionate, self-taught Cloud & DevOps Engineer specializing in AWS enterprise architectures, Serverless Workloads, CI/CD automation, and Machine Learning Infrastructures. Currently a Vocational High School (SMK) student majoring in Computer and Network Engineering, I thrive on designing highly available production environments and robust cross-regional secure infrastructures.

---

### 🔒 Note on Enterprise Architecture & Source Code
> *Due to the proprietary nature of my enterprise-grade cloud architectures and to prevent unauthorized replication, source codes and topology diagrams are kept strictly private. Detailed architecture portfolios and topological diagrams are available exclusively upon direct request for professional evaluation and technical interviews.*

---

### 🏆 National Achievements & Awards
* 🥇 **1st Place, LKS Cloud Computing (East Java, 2026)**
* 🥇 **1st Place, NETCOMP 4.0 (Universitas Gadjah Mada, 2026)**
* 🥇 **1st Place, IONIC (Politeknik Elektronika Negeri Surabaya, 2025)**

---

### 🚀 Enterprise & Complex Architecture Projects

#### 1. Security Reliability on EKS (Attacker vs Defender Simulation)
* **Tech Stack:** AWS EKS, Istio, Falco, Vault, AWS WAF, NLB, Ingress, Locust, OWASP ZAP, Chaos Mesh, SQS, SNS, DynamoDB, RDS.
* **Detailed Architecture:** * **Defender Infrastructure:** Architected a highly secure Amazon EKS cluster exposed via NLB and Ingress. Implemented **Istio** for service mesh, **Falco** for runtime threat detection, and **Vault** for secrets management. Deployed secure pods including transaction workers processing queues via **SQS** and **SNS**, connected to **RDS** and **DynamoDB**. Traffic is filtered through a dedicated WAF worker pod.
  * **Attacker Infrastructure:** Engineered a separate simulation environment using NLB and EKS to launch controlled attacks. Integrated **Locust** for load generation, **OWASP ZAP** for vulnerability scanning, and **Chaos Mesh** for chaos engineering to validate the defender's cluster reliability and auto-recovery capabilities.

#### 2. HealthTech Monitoring System with ML Integration
* **Tech Stack:** AWS Elastic Beanstalk, S3, Lambda, Amazon Redshift, SageMaker, ECS, ALB, EC2 (Ollama), RDS Aurora PostgreSQL, DynamoDB.
* **Detailed Architecture:** * **Data Pipeline:** Ingested external health datasets via Kaggle API deployed on **Elastic Beanstalk**, storing raw data in **S3**. A trigger invokes **Lambda** to process and load structured data into **Amazon Redshift** and **RDS Aurora PostgreSQL**. DynamoDB handles real-time logs which are also synced to Redshift.
  * **Machine Learning Ops:** Utilized **Amazon SageMaker Training** to build predictive health models. Inference is handled by a dedicated **Lambda** attached to **EFS** (to load large models), and a custom **EC2** running **Ollama** for advanced processing. The frontend interacts via an **ALB** routing to **ECS** containers.

#### 3. AI-Driven Incident Management (Machine Learning Incident)
* **Tech Stack:** EventBridge Scheduler, CloudWatch (Logs, Alarms), SNS, Kinesis Data Streams, Firehose, S3, Glue, Athena, SageMaker, DynamoDB, EFS, ECS, ALB, GitHub Actions, CodeDeploy.
* **Detailed Architecture:** * Configured **EventBridge Schedulers** to trigger incident simulations via **Lambda**. 
  * Captured system events using **CloudWatch Logs**, utilizing Subscription Filters to stream logs into **Kinesis Data Streams** and **Firehose**, delivering them to **S3**. 
  * Leveraged **Glue** and **Athena** for log querying, while **SageMaker** runs anomaly detection models. 
  * Deployed a highly available API on **ECS** behind an **ALB** to serve incident data stored in **DynamoDB** and **EFS**. 
  * Fully automated infrastructure and application updates via **GitHub Actions** integrated with **AWS CodeDeploy (ECS)** for Blue/Green deployments triggered by **CloudWatch Alarms** (Auto-rollback enabled).

#### 4. E-Commerce with Integrated Bank Infrastructure (Dual Region)
* **Tech Stack:** Multi-Region AWS, Cognito, Amplify, API Gateway, WAF, Lambda, Secrets Manager, DynamoDB, RDS, S3, Step Functions, Amazon Rekognition, Textract, SNS.
* **Detailed Architecture:** * Designed a **Dual-Region Active** architecture for strict High Availability and Disaster Recovery compliance.
  * User authentication and identity verification (KYC) are handled by **Cognito**, orchestrated by **Step Functions** integrating **Amazon Rekognition** (face liveness) and **Textract** (ID card OCR).
  * Secure endpoints are exposed via **API Gateway** protected by **AWS WAF**. Core banking transactions are processed by **Lambda**, utilizing **Secrets Manager** for credentials, with robust data persistence across **DynamoDB** and **RDS**.

#### 5. Autonomous Mobile Robot Cloud Infrastructure
* **Tech Stack:** AWS IoT Core, Kinesis, Firehose, S3, Glue, Athena, SageMaker, SNS, Lambda, DynamoDB, ALB, EC2 (Ollama), Cognito, Amplify.
* **Detailed Architecture:** * Established a secure, bi-directional communication channel for physical robots using **AWS IoT Core**. 
  * Massive real-time telemetry data is streamed via **Kinesis** and **Firehose** into a Data Lake (**S3**), queried using **Glue** and **Athena**. 
  * Advanced sensor data is inferred using **SageMaker** and an **EC2-hosted Ollama** instance. 
  * Operators monitor robot status via a React frontend hosted on **Amplify** and authenticated by **Cognito**, pulling real-time states from **DynamoDB** via **ALB** and **Lambda**. Critical hardware alerts trigger immediate **SNS** notifications.

#### 6. E-Commerce Flash Sale Architecture
* **Tech Stack:** 2x Amplify (Admin/Client), Cognito, ECS, Redis (ElastiCache), CloudWatch, Secrets Manager, API Gateway, Lambda, EventBridge, Elastic Beanstalk, S3, RDS, Step Functions.
* **Detailed Architecture:** * Built to handle extreme traffic spikes using **Redis** for high-speed caching and inventory locking. 
  * The frontend consists of isolated Admin and Client portals hosted on **Amplify**. 
  * The core Flash Sale API runs on scalable **ECS** tasks. Background order processing and queue management are orchestrated by **Step Functions**, **EventBridge**, and **Elastic Beanstalk** workers to ensure zero transaction loss during peak concurrency. Data persistence and automated backups are handled by **RDS** and **S3**.

#### 7. Sales Machine Learning Analytics
* **Tech Stack:** EC2, CloudWatch, SNS, Lambda, S3, Glue, Athena, Redshift, SageMaker Studio, Kinesis, Firehose, DynamoDB, ECS, ALB, CodeDeploy, GitHub Actions.
* **Detailed Architecture:** * Developed a traffic simulator on **EC2** to generate real-time sales data. 
  * Data is streamed through **Kinesis** and **Firehose** into an **S3** Data Lake. **Glue** catalogs the data for **Athena** and data warehouse analytics in **Redshift**.
  * Data scientists utilize **SageMaker Studio** to build forecasting models. The production API runs on **ECS** behind an **ALB**, with fully automated CI/CD pipelines pushing updates via **GitHub Actions** and **CodeDeploy (ECS & EC2)**.

#### 8. Loux Bank Core System
* **Tech Stack:** Cognito, RDS, DynamoDB, SQS, S3, SNS, EventBridge, Step Functions, Amazon Rekognition, Amplify.
* **Detailed Architecture:** Developed a core banking prototype focused on asynchronous transaction processing. Utilized **SQS** to decouple transaction requests, processed by **Step Functions**. Integrated **Amazon Rekognition** for secure user onboarding and **SNS** for OTP and transaction alerts.

---

### 🌐 Mid-Level & Serverless Applications

#### 9. EventBuddy
* **Architecture:** Full serverless event management platform. User access is secured via **Cognito**. The React frontend is deployed on **Amplify**. Complex ticketing transactions are decoupled using **SQS** queues, processed by **Lambda**, and stored relationally in **RDS** and NoSQL in **DynamoDB**. Media files are stored in **S3**, with email/SMS confirmations handled by **SNS**.

#### 10. Coding Platform System
* **Architecture:** Architected a remote code execution platform. Code submission requests hit an **API Gateway** and are queued in **SQS**. Scalable **EC2 Workers** consume the queue to compile/run the code. Scheduled maintenance and container cleanups are triggered by **EventBridge Scheduler**. Progress and results are stored in **DynamoDB** and **RDS**.

#### 11. Karaoke Reservation System
* **Architecture:** A monolithic-to-microservices transitional architecture. The frontend runs on **EC2** behind an **Application Load Balancer (ALB)**. Reservation logic is processed through **API Gateway** and **Lambda**, utilizing **RDS** for booking schedules and **DynamoDB** for session caching.

#### 12. Basic Product CRUD Platform
* **Architecture:** Serverless REST API utilizing **Amplify** for frontend hosting, **API Gateway**, **Lambda** for business logic, and **RDS** for relational data mapping.

#### 13. Debt Tracking App (CRUD Debt)
* **Architecture:** Ultra-low latency serverless application leveraging **DynamoDB** for fast read/write tracking of financial ledgers. Exposed via **API Gateway** and **Lambda**, with a frontend hosted on **AWS Amplify**.

---

### 📫 Connect with me:
* **Email:** feriadiputra6@gmail.com
* **LinkedIn:** [LinkedIn Profile](https://www.linkedin.com/in/feriadi-p-035a133b2/)

⭐️ *From Blitar, East Java to the Cloud!*
