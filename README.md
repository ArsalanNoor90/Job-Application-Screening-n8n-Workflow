# Job Application Tracker & Screening — n8n Workflow

An automated HR screening workflow built with n8n that ingests candidate responses from Google Forms, automatically classifies experience levels, checks for duplicate applications, logs data into Google Sheets, and sends tailored email communications via Gmail.

---

## ⚙️ What It Does

> 💡 **Workflow Overview**
> 
> * **1. Application Ingestion:** Listens to incoming Google Forms entries in real-time.
> * **2. Experience Classification:** Automatically tags candidate profiles as **Junior**, **Mid Level**, or **Experienced**.
> * **3. Duplicate Guard:** Queries the master Google Sheet to prevent double-processing.
> * **4. Automated Communication:** Automatically routes **Interview Invites** to qualified candidates and **Keep-on-File Emails** to junior applicants.

---

## 🖼️ System Screenshots

| Workflow Architecture | Application Form & Database |
| :---: | :---: |
| ![n8n Workflow](Screenshot%202026-09-14%20195127.png) | ![Google Form](Screenshot%202026-09-14%20195348.png) |

| Master Database Ledger |
| :---: |
| ![Google Sheets](Screenshot%202026-09-14%20195528.png) |

---

## ⚡ Features & System Capabilities

| Feature | Description |
| :--- | :--- |
| 📥 **Application Ingestion** | Triggers automatically whenever a new Google Form application is submitted. |
| 🏷️ **Experience Classification** | Automatically categorizes applicants into **Junior/Entry**, **Mid Level**, and **Experienced** tiers. |
| 🛡️ **Duplicate Prevention** | Checks existing records in Google Sheets to avoid double-processing candidates. |
| 📊 **Centralized Database** | Logs structured candidate details directly into Google Sheets. |
| 🔀 **Dynamic Communication** | Automatically dispatches Interview Invites or Keep-on-File retention emails via Gmail. |

---

## 📋 Candidate Data Fields

```text
┌─────────────────────────┬────────────────────────────────────────────────────────────┐
│ Field Name              │ Field Description                                          │
├─────────────────────────┼────────────────────────────────────────────────────────────┤
│ 👤 Full Name            │ Candidate's complete name                                  │
│ 📧 Email                │ Candidate's contact email address                          │
│ 📞 Phone Number         │ Contact number for candidate reachout                      │
│ 🎯 Position Applying    │ Applied job role (e.g., Logistics Manager)                │
│ ⏳ Years of Experience  │ Raw years entered in the form                              │
│ 🏷️ Experience Category  │ Classified tier: Junior / Mid Level / Experienced          │
│ 📌 Status               │ Decision status: "Interview Eligible" or "Keep On File"   │
└─────────────────────────┴────────────────────────────────────────────────────────────┘

---

## 🛠️ Tech Stack & Integration Ecosystem

| Technology / Tool | Category | Role in Workflow |
| :--- | :--- | :--- |
| ⚡ **n8n** | Orchestration | End-to-end workflow automation & conditional execution logic |
| 📋 **Google Forms** | Ingestion | Captures structured candidate applications and data inputs |
| 📊 **Google Sheets** | Database | Centralized Master Application Ledger for tracking & deduplication |
| 📧 **Gmail API** | Communication | Automated notification dispatching for interviews and updates |
| 📜 **JavaScript (ES6+)** | Logic Engine | Dynamic parsing, string cleaning, and integer experience mapping |

---

## 🔄 Workflow Overview & Execution Logic

| Step | Phase | Action / Node Executed | Description |
| :---: | :--- | :--- | :--- |
| **01** | **Ingestion** | `Google Forms Trigger` | Listens for new candidate submission payloads in real time. |
| **02** | **Preparation** | `Code Node (Data Prep)` | Cleans string variables and extracts integer values for experience fields. |
| **03** | **Classification**| `Switch Node (Logic)` | Evaluates experience tier (`Junior`, `Mid Level`, `Experienced`). |
| **04** | **Deduplication** | `Google Sheets (Read)` | Scans master ledger for matching emails to prevent duplicate entries. |
| **05** | **Storage** | `Google Sheets (Append)`| Records validated candidate entries into the centralized HR database. |
| **06** | **Routing** | `Gmail Node` | Dispatches **Interview Invites** to qualified tiers or **Retention Emails** to junior applicants. |

---

## 🚀 Setup & Execution Guide

| Step | Section | Instruction |
| :---: | :--- | :--- |
| **01** | **Import Workflow** | Open n8n ➔ Click **Import from file** ➔ Select `Job Application Tracker & Screening Workflow.json`. |
| **02** | **Add Credentials** | Configure **Google OAuth2** (for Forms & Sheets) and **Gmail OAuth2** in n8n credential settings. |
| **03** | **Configure Nodes** | Connect your specific Google Form ID, Google Sheet Ledger ID, and HR Sender Gmail address. |
| **04** | **Activate Workflow**| Toggle the workflow switch to **Active** (Top Right) to start handling live applications. |

---

## 💡 Practical Use Cases

| Industry / Use Case | Problem Solved | Business Impact |
| :--- | :--- | :--- |
| **High-Volume Recruitment** | Manual filtering of hundreds of daily applicant forms | Saves ~15+ hours/week of HR screening time |
| **Agile Startup Hiring** | Inconsistent candidate follow-ups and lost records | 100% automated response rate within seconds of submission |
| **Agency Candidate Tracking**| Double-submission of resumes by same candidate | Zero redundant entries in master client database |

---

## 💬 Example Workflow Conversation Flow

```text
[Candidate Submits Form]
 ├── Name: Jane Doe
 ├── Position: Logistics Manager
 └── Experience: 4 Years

[n8n Engine Processing]
 ├── Data Cleaned: Experience mapped to 4 (Integer)
 ├── Category Assigned: "Mid Level"
 └── Deduplication Check: Email clean (No previous entries found)

[Automated Execution]
 ├── Database: Row added to Google Sheets Master Ledger
 └── Communication: Gmail dispatches "Interview Invitation & Next Steps" email

---

## 🎬 Live Demo Video

| Platform | Access Link | Walkthrough Coverage |
| :---: | :---: | :--- |
| 🚀 **LinkedIn** | [▶️ Watch Loom Demo Video][(YOUR_LINKEDIN_LOOM_POST_URL](https://www.linkedin.com/posts/arsalan-noor-1510492bb_n8n-automation-hrtech-activity-7505220191522459648-h2AT?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEy28Y0ByakjFKAlhxlwGieeh2Fc8Djsg8s)) | Full end-to-end execution: Google Form submission ➔ n8n processing ➔ Sheet logging |


📜 LicenseMIT License — Free to modify, use, and distribute for commercial or personal projects.











