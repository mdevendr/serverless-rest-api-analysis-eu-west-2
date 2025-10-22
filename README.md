# ☁️ Serverless REST API Architecture — Technical Cost & Performance Analysis (AWS eu-west-2)

## 📘 Objective
This whitepaper provides a **technical and cost–performance analysis** of an **AWS Serverless REST API Architecture** designed for scalable, secure, and cost-efficient workloads in the **eu-west-2 (London)** region.

It compares **Serverless (Lambda-based)** and **EC2-based** architectures across **cost, latency, resilience, and compliance alignment**, helping architects and engineering teams make informed design decisions.

**Key goals:**
- Quantify **cost efficiency (40–60% lower)** vs EC2-based compute  
- Measure **performance (<50 ms average latency)** at regional scale  
- Map controls to **Well-Architected, DORA, PCI DSS, and ISO 27001** frameworks  
- Provide a **reference implementation blueprint** for serverless adoption

---

## 🏗️ Architecture Overview
The solution follows a **fully serverless, event-driven design** using managed AWS services.

### 🔹 Core Components
- **Amazon API Gateway** – RESTful API entry point, request routing, and authentication via Cognito  
- **AWS Lambda** – Stateless compute functions for token validation, business logic, and CRUD operations  
- **Amazon DynamoDB** – NoSQL backend with on-demand scaling and encryption at rest  
- **AWS Secrets Manager** – Secure credential storage with KMS encryption  
- **Amazon CloudWatch** – Centralized logging, metrics, and alerting  
- **Amazon S3** – Static asset hosting and backup storage  
- **AWS Certificate Manager (ACM)** – SSL/TLS certificate provisioning for API Gateway endpoints  
- **AWS IAM** – Fine-grained access control and least-privilege permissions  

### 🔸 Optional Enhancements
- **AWS X-Ray** for distributed tracing and latency analysis  
- **VPC Endpoints** for private service connectivity and data-in-transit protection  

---

## 📊 Key Metrics

| Metric | Lambda (Serverless) | EC2 (Traditional) | Insight |
|:-------|:--------------------|:------------------|:--------|
| **Average Latency** | < 50 ms (regional) | ~120–150 ms | Serverless achieves lower latency under burst load |
| **Cost Efficiency** | 40–60 % lower | Baseline | Pay-per-use eliminates idle compute cost |
| **Availability** | 99.99 % (Multi-AZ) | 99.9 % (Manual) | Built-in regional resilience |
| **Scalability** | Instant, per-request | Manual / ASG delay | Lambda scales to zero and up instantly |
| **Operational Overhead** | Minimal | High | AWS manages patching, scaling, monitoring |
| **Compliance Ref.** | DORA, PCI DSS, ISO 27001 | Manual | Managed compliance at service level |

---

## 🔐 Compliance & Governance
The design aligns with major compliance and operational-resilience standards:

- **DORA** – Continuous availability, incident management, and fault tolerance  
- **PCI DSS** – Encryption, key rotation, network segmentation, IAM boundaries  
- **ISO 27001** – Logging, encryption in transit / at rest, policy enforcement  
- **AWS Well-Architected Framework** – Security | Reliability | Performance | Cost Optimization | Operational Excellence  

---

## 🧠 Key Insights
- **Serverless-first architectures** yield measurable cost and performance gains for variable workloads  
- **IAM + KMS integration** delivers compliance-grade security with minimal admin effort  
- **Cold-start mitigation** and **event-driven scaling** improve both performance and resilience  
- **Well-Architected + Compliance mapping** enables governance alignment out of the box  

---

## 👤 Author
**Mahesh Devendran**  
*Cloud Architect | AWS | Azure | GCP | Serverless | Security*  

- 📍 London, United Kingdom (eu-west-2)  
- 🌐 [LinkedIn Profile](https://www.linkedin.com/in/mahesh-devendran-83a3b214)  
- 📧 Contact: mahesh.devendran@gmail.com 
- 🧾 Whitepaper: **Serverless_Technical_Analysis_eu-west-2.pdf**

---

## 📂 Repository Structure
/whitepaper
└── Serverless_Technical_Analysis_eu-west-2.pdf
/diagrams
└── architecture.png
README.md
