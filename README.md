# Job Application Tracker & Screening — n8n Workflow

An automated HR screening workflow built with n8n that ingests candidate responses from Google Forms, automatically classifies experience levels, checks for duplicate applications, logs data into Google Sheets, and sends tailored email communications via Gmail.

---

## ⚙️ What It Does
+---------------------------------------------------------------------------------+
|                                WORKFLOW PIPELINE                                |
+---------------------------------------------------------------------------------+
|  [ 📑 Google Form Submission ]                                                  |
|                 │                                                               |
|                 ▼                                                               |
|  [ ⚙️ Data Preparation & Cleaning ]                                              |
|                 │                                                               |
|                 ▼                                                               |
|  [ 🏷️ Experience Classification ] ─── ( Junior / Mid / Experienced )             |
|                 │                                                               |
|                 ▼                                                               |
|  [ 🛡️ Duplicate Candidate Check ] ─── ( Query Google Sheets Ledger )             |
|                 │                                                               |
|                 ▼                                                               |
|  [ 📊 Append Record to Google Sheets ]                                          |
|                 │                                                               |
|                 ├───────────────────────────────┐                               |
|                 ▼                               ▼                               |
|   [ 📩 Send Interview Invite ]      [ 📥 Send Keep-on-File Email ]              |
|     (If Experience >= Mid)            (If Experience == Junior)                 |
+---------------------------------------------------------------------------------+


🖼️ System Screenshots
┌─────────────────────────────────────────────────────────────────────────────────┐
│ 1. n8n Workflow Canvas Architecture                                            │
└─────────────────────────────────────────────────────────────────────────────────┘
┌─────────────────────────────────────────────────────────────────────────────────┐
│ 2. Application Form & Master Google Sheets Ledger                               │
└─────────────────────────────────────────────────────────────────────────────────┘

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





