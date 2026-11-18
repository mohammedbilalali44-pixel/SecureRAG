## SecureRAG
SecureRAG is a security-focused Retrieval-Augmented Generation (RAG) proof of concept designed to demonstrate how sensitive enterprise information can be protected using layered security controls.

The project combines document retrieval, risk analysis, Role-Based Access Control (RBAC), Data Loss Prevention (DLP), query filtering, and security monitoring to prevent confidential data exposure through AI-powered systems.

## Key Features
Retrieval-Augmented Generation (RAG)
ChromaDB Vector Database
Role-Based Access Control (RBAC)
Data Loss Prevention (DLP)
Risk-Based Query Classification
Sensitive Query Detection
Policy Enforcement Engine
Security Audit Logging
Security Monitoring Dashboard
Flask Web Interface

## Architecture
![SecureRAG Architecture](screenshots/01_SecureRAG_Architecture.png)

## Document Ingestion

The ingestion engine processes uploaded documents, extracts content, generates vector embeddings, and stores them in ChromaDB for retrieval.

![Document Ingestion](screenshots/02_Document_Ingestion.png)

## Demonstrating the Security Risk

Before implementing security controls, the model was able to retrieve and expose sensitive information contained within indexed documents.

![Insecure Model Response](screenshots/03_Insecure_Model_Response.png)

## Data Loss Prevention (DLP)

SecureRAG applies data loss prevention controls to detect and redact sensitive information before it is returned to users.

![WebUI DLP Redaction](screenshots/04_WebUI_DLP_Redaction.png)

## Role-Based Access Control (RBAC)

Unauthorized requests are blocked based on user permissions and risk classification.

![WebUI Access Denied](screenshots/05_WebUI_Access_Denied.png)

![CLI RBAC Access Denied](screenshots/06_CLI_RBAC_Access_Denied.png)

## Security Enforcement

Multiple security controls work together to classify risk, redact sensitive data, and block prohibited requests.

![DLP RBAC Enforcement](screenshots/07_DLP_RBAC_Enforcement.png)

![Multi-Layer Security Enforcement](screenshots/08_MultiLayer_Security_Enforcement.png)

## Monitoring and Auditing

All security-relevant events are logged to support investigation, compliance, and operational monitoring.

![Security Monitoring Dashboard](screenshots/09_Security_Monitoring_Dashboard.png)

## Sensitive Query Protection

Credential harvesting and other high-risk requests are automatically detected and blocked.

![Sensitive Query Blocking](screenshots/10_Sensitive_Query_Blocking.png)
