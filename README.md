# Real Estate Intelligent Lease & Operations Analytics Platform

An enterprise-grade, **Zero-Trust AWS Generative AI & Lakehouse Platform** engineered to automate document intelligence, vendor spend guardrails, and operational analytics across enterprise real estate portfolios.

Built on **Amazon Bedrock AgentCore**, **OpenSearch Serverless RAG**, **AWS Step Functions HITL State Machines**, and an **AWS Data Lakehouse (Glue, Athena, QuickSight)**, this architecture delivers secure role-based document retrieval, automated lease contract parsing, and financial risk controls.

---

## Executive Summary & Strategic Context

Enterprise real estate investment and property management organizations handle thousands of unstructured documents—lease agreements, vendor invoices, due diligence reports, maintenance logs, and regional compliance filings. Property managers and asset leaders spend thousands of manual hours searching across decentralized silos, leading to delayed decision-making, vendor overcharges, and operational inefficiencies.

This platform bridges unstructured property data with executive decision-making through a **4-Component ROI Engine** and **CPMAI-governed Phase Gates**, delivering:
* **7.5-Month Payback Period** with an estimated **55,000+ annual operational savings**.
* **200%+ 2-Year ROI** by eliminating manual contract audits and reducing vendor invoice processing overhead by 85%.
* **Zero-Trust RBAC Isolation**, ensuring property managers, regional leads, and legal counsel only access document passages permitted by their explicit IAM security roles.

---

## System Architecture

The architecture combines cloud-native AI document processing with deterministic workflow governance and serverless analytics.

### Architecture Diagram (Native GitHub Mermaid Rendering)



> **Visual Architectural Diagram:** A high-resolution architecture diagram () is included in the assets directory.

---

## Problem Discovery & 3-Year Build vs. Buy vs. Partner TCO

Applying CPMAI Phase I (*Business Understanding*) discovery craft, this project evaluated three deployment models for real estate portfolio AI transformation:

| Evaluation Criteria | Option A: Off-the-Shelf SaaS (Buy) | Option B: Custom AWS Hybrid Build | Option C: Partner Outsourcing |
| :--- | :--- | :--- | :--- |
| **3-Year Total Cost of Ownership (TCO)** | 50,000+ (50k/yr recurring per seat) | **35,000** (20k initial + ~k/yr ops) | 80,000+ (25k/yr retainer) |
| **Data Ownership & IP Rights** | Third-party vendor lock-in | **100% Enterprise IP & Data Control** | Shared partner lock-in |
| **Security & RBAC Controls** | Coarse tenant-level security | **Granular IAM & Passage-Level Isolation** | Partner-managed access |
| **Custom Integration** | Rigid proprietary APIs | **Native Lakehouse (Glue / Athena / QuickSight)** | Custom API wrappers |
| **3-Year Net Savings** | Baseline | **+15,000 TCO Advantage** | +0,000 |

**Strategic Decision:** Option B (AWS Hybrid Build) was selected for its superior long-term TCO, zero vendor lock-in, and native compatibility with enterprise data governance standards.

---

## Technical Component Deep-Dive

### 1. Document Ingestion & Feature Extraction
* **Amazon Textract & S3:** Ingests PDF leases, TIFF invoices, and scanned maintenance records, extracting raw key-value pairs, tables, and structural text layouts.
* **AWS Glue ETL:** Normalizes document metadata (Property ID, Unit Type, Lease Start/End, Vendor ID) into structured Apache Parquet formats stored in S3 data lake tiers.

### 2. Cognitive Retrieval & Zero-Trust RBAC
* **Amazon Bedrock AgentCore:** Coordinates multi-step query planning, leveraging Foundation AI models for natural language lease abstraction and anomaly detection.
* **OpenSearch Serverless Vector Engine:** Maintains high-dimensional embeddings generated via Amazon Titan Text Embeddings.
* **IAM Passage Isolation:** Applies attribute-based security filters directly at vector query execution time, ensuring on-site managers only access assets within their assigned property region.

### 3. Human-in-the-Loop (HITL) Policy Safeguards
* **AWS Step Functions:** Enforces policy-as-code guardrails. Any automated recommendation involving financial commitments or vendor approvals above ,000 triggers a mandatory HITL notification to regional asset managers.

### 4. Data Lakehouse & Executive BI
* **Amazon Athena & QuickSight:** Enables serverless SQL querying over raw and processed real estate records, feeding real-time executive dashboards for Net Operating Income (NOI), lease expiration cliffs, and vendor variance analysis.

---

