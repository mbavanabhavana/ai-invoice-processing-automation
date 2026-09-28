# 🤖 AI Invoice Processing & Duplicate Detection Automation

An automated invoice processing workflow built with **n8n, Gmail, AI, and Google Sheets**.

The system receives invoice emails, extracts invoice information, validates the data, checks whether the invoice has already been processed, and automatically stores new invoices in Google Sheets.

---

## 📌 Project Overview

Manual invoice processing can take time and may lead to duplicate entries.

This project automates the process:

**Gmail → AI Invoice Processing → Invoice Validation → Duplicate Check → Google Sheets**

The workflow also prevents the same Gmail message from being inserted into the spreadsheet more than once.

---

## 🚀 Features

- 📧 Automatic Gmail invoice processing
- 🤖 AI-based invoice data extraction
- 📄 PDF invoice parsing
- ✅ Invoice data validation
- 🔍 Duplicate invoice detection
- 📊 Automatic Google Sheets storage
- 🛑 Prevents duplicate entries
- ⚡ Automated workflow execution
- 🔄 Published n8n workflow

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **n8n** | Workflow automation |
| **Gmail** | Receive invoice emails |
| **AI / LLM** | Extract and process invoice information |
| **JavaScript** | Data validation and transformation |
| **Google Sheets** | Store invoice records |
| **PDF** | Invoice input format |

---

## 🔄 Workflow

```text
Gmail
   ↓
Invoice Message
   ↓
PDF JSON Parser
   ↓
Invoice Validation
   ↓
Get Row(s) in Google Sheets
   ↓
IF2 – Duplicate Check
   ↓
 ┌───────────────┴───────────────┐
 │                               │
TRUE                            FALSE
 │                               │
Duplicate                       New Invoice
 │                               │
STOP                            Append Row
                                 ↓
                           Google Sheets
