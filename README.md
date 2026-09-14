# Job Application Tracker & Screening — n8n Workflow

An automated HR screening workflow built with n8n that ingests candidate responses from Google Forms, automatically classifies experience levels, checks for duplicate applications, logs data into Google Sheets, and sends tailored email communications via Gmail.

---

## What It Does

```text
[ Google Form ] ➔ [ Data Prep ] ➔ [ Experience Classification ]
                                              │
                                              ▼
[ Email Alerts ] ◄─ [ Duplicate Check ] ◄─ [ Data Deduplication ]


---

## Screenshots

### Workflow Architecture
![n8n Workflow](Screenshot 2026-09-14 195127.png)

### Google Form & Database Setup
![Google Form](Screenshot 2026-09-14 195348.png)
![Google Sheets Database](Screenshot 2026-09-14 195528.png)

---

## License

MIT — Free to use and customize.


---

## Features

| Feature | Description |
| :--- | :--- |
| **Application Ingestion** | Triggers automatically on Google Forms submission. |
| **Experience Classification** | Automatically labels candidates (Junior/Entry, Mid Level, Experienced). |
| **Duplicate Prevention** | Checks existing applications to prevent double-processing. |
| **Centralized Database** | Appends clean data directly into Google Sheets. |
| **Dynamic Email Routing** | Sends interview invites to qualified applicants & retention emails to junior profiles. |

---

## Candidate Data Fields

| Field | Description |
| :--- | :--- |
| **Full Name** | Candidate's complete name |
| **Email** | Applicant email address |
| **Phone Number** | Contact number |
| **Position** | Applied position (e.g., Logistics Manager, Dispatch Officer) |
| **Experience** | Raw experience input & classified category |
| **Status** | Candidate routing status (Interview Eligible vs Keep On File) |



