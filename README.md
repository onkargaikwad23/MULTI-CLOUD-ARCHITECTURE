# MULTI-CLOUD-ARCHITECTURE

"COMPANY": CODTECH IT SOLUTIONS

*NAME* : Onkar Gaikwad

*INTERN ID*: CT04DF734

*DOMAIN*: Cloud Computing

*DURATION*: 4 WEEEKS

*MENTOR*: NEELA SANTOSH

Descripription-

# 🌐 Task 3 – Multi-Cloud Architecture Design

## 📌 Objective

Design a **multi-cloud architecture** where services are **distributed across two cloud providers**, ensuring **interoperability** and cross-cloud communication.

This architecture demonstrates how two major cloud platforms—**Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**—can be integrated to create a resilient, distributed system.

---

## 🛠️ Tools & Technologies Used

- **AWS**: S3 (for storage), Lambda (for compute)
- **GCP**: Cloud Function (for data processing or endpoint API)
- **API Gateway (optional)**: To enable API-based cross-cloud communication
- **IAM roles and service accounts**: For secure access

---

## 🖼️ Architecture Description

### ⚙️ Setup Overview:

- **AWS Side**:
  - An S3 bucket stores uploaded files.
  - An AWS Lambda function is triggered when a file is uploaded.
  - Lambda makes a REST API call to a **GCP Cloud Function**.

- **GCP Side**:
  - Cloud Function receives the request and processes it (e.g., logs or stores metadata in Firestore).
  - Responds with a status back to Lambda or logs result.

### 📡 Data Flow:

1. File uploaded to `codtech-cloud-harsh-bucket` in AWS S3.
2. AWS Lambda function is automatically triggered via S3 event.
3. Lambda sends a `POST` request to a public GCP Cloud Function endpoint with the file metadata (e.g., filename, timestamp).
4. GCP Cloud Function logs/handles the data (e.g., stores in Firestore or BigQuery).

---

## 📷 Screenshots / Evidence (in `screenshots/` folder)

- AWS S3 bucket with file upload
- AWS Lambda trigger configuration
- Lambda function code with HTTP request to GCP
- GCP Cloud Function deployment page
- Console logs showing successful request from AWS
- Architecture diagram (in PNG or PDF)

---

## 🔒 Security Measures

- IAM role for Lambda with permission to access S3 and make external HTTPS requests.
- GCP Cloud Function configured with an HTTPS trigger and optional API key validation.
- CORS and HTTPS enforced for secure transmission.

---

## 📎 Deliverable (Per Instructions)

✔️ **Documentation**:
- This `README.md` serves as the main report, explaining setup, architecture, and implementation.
- Architecture diagram (`architecture-diagram.png`) visually presents the full flow.

✔️ **Demo**:
- A sample file uploaded to S3 triggers the Lambda.
- Logs from GCP show the function receiving and handling the request.

✔️ **Interoperability**:
- Verified communication between AWS Lambda and GCP Cloud Function via REST APIs.

---

## 💡 Skills Gained

- Understanding how to integrate two cloud platforms
- Designing secure cross-cloud communication
- Serverless function chaining (S3 → Lambda → GCP)
- Building scalable, fault-tolerant systems

---

## ✅ Conclusion

This task illustrates real-world scenarios where enterprises use a **multi-cloud approach** to reduce vendor lock-in, optimize costs, and build highly available services. By combining AWS and GCP services into a single workflow, I gained hands-on experience with distributed cloud computing and secure inter-service communication.

This architecture is scalable, cost-effective, and modular—demonstrating modern cloud design principles in action.

#output

