# 🧠 Mental Health Assessment Certificate Generator & Distribution System

An end-to-end automated system for evaluating mental health and stress levels. Powered by **Google Workspace**, **n8n**, **JavaScript**, **PDFShift API**, and **Gmail API**.

---

## 📝 Try the Survey & Sample Result

| 📲 Try the Survey (QR Code) | 📄 Sample Assessment Report |
| :---: | :---: |
| ![Survey QR Code](https://github.com/user-attachments/assets/87fa9f18-910c-49d9-8afc-030fae3fb440) | ![Certificate Preview](https://github.com/user-attachments/assets/a4a6db1f-d28d-4ae7-acc4-1cea168350c8) |

> 💡 *Scan the QR code to take the live survey or view the automatically generated color-coded PDF report.*

---

## 🚀 Project Overview

Mental health awareness is crucial, yet many individuals face barriers to early pre-screening due to cost, privacy concerns, or lack of access. 

This project delivers an automated **Mental Health & Stress Level Assessment System**. It streamlines the process from user submission to real-time scoring, custom PDF report generation, and automated email delivery. Designed as a sustainable, privacy-focused pre-screening tool for enterprise **HR departments**, **educational institutions**, and **healthcare clinics**.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Intake:** Google Forms & Google Sheets
* **Workflow Automation:** n8n (Self-hosted / Cloud)
* **Custom Scoring Engine:** JavaScript (n8n Code Node)
* **Document Generation:** HTML5, CSS3, and PDFShift REST API
* **Email & Distribution:** Gmail API
* **Database & Logging:** n8n Data Table / Google Sheets API

---

## ✨ Key Features

* **⚡ Real-time Event Triggering:** Instantly detects new form entries using Google Sheets `rowAdded` triggers.
* **🎯 Multi-Factor Scoring Algorithm:** Evaluates Likert-scale and binary responses to categorize stress into 3 risk tiers:
  * 🟢 **Normal (อยู่ในเกณฑ์ปกติ):** Wellness maintenance and positivity encouragement.
  * 🟠 **Caution (ควรเฝ้าระวังและดูแลตนเอง):** Stress-relief, digital detox, and self-care steps.
  * 🔴 **Action Required (ควรได้รับการประเมินเพิ่มเติมโดยผู้เชี่ยวชาญ):** Guidance for professional consultation & Mental Health Hotline (1323) contact info.
* **🌐 Dynamic & Bilingual Reports:** Injects user data into dynamic HTML/CSS templates, styling reports with severity-based color coding (Green/Orange/Red) and dual-language advice (Thai/English).
* **✉️ Automated Email Dispatch:** Delivers a warm, personalized email with the generated PDF report attached.
* **📊 Audit Logging Pipeline:** Generates a unique Assessment ID (`MH-{timestamp}`) and records execution logs into a database table for tracking and compliance.

---

## ⚙️ Workflow Architecture

```text
[ Google Form ] ➔ [ Google Sheets ] ➔ [ n8n Trigger ]
                                            │
                                            ▼
[ Database Log ] ◄── [ Gmail API ] ◄── [ PDFShift API ] ◄── [ HTML Render ] ◄── [ JS Scoring Algorithm ]

---

## Project Type

University Team Project
