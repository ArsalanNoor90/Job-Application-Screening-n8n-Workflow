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






