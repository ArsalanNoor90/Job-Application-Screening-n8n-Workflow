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





