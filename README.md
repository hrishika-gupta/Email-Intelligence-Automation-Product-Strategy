# 📬 Email Intelligence Automation with Python

A Python-based pipeline built to process and analyze 7,000+ `.eml` client inquiry emails for product insight discovery at Afforest. This tool helped automate lead data extraction and convert unstructured email content into actionable insights for product development and sales strategy.

---

## 🚀 Project Overview

During my internship at Afforest, I was tasked with uncovering key patterns and regions of interest within 7,000+ inbound email queries received by the team. These emails were crucial for informing the design of future products but were trapped in `.eml` files with no structured access.

To solve this, I built a **complete automation pipeline** that:
- Extracts email metadata (sender, date, subject)
- Parses and cleans full body content
- Detects and validates **phone numbers** using `phonenumbers`
- Identifies **locations** via Named Entity Recognition (`spaCy`)
- Compiles all insights into a clean, analyzable `.csv` format

---

## 🔧 Tech Stack

- `Python 3.10+`
- `email` (standard library)
- `re` (regex)
- `phonenumbers`
- `spaCy` (`en_core_web_sm`)
- `csv`
- `.eml` file parsing

---

## 🧠 Key Features

✅ Parse `.eml` email files  
✅ Extract sender name, email, subject, date  
✅ Clean + extract full plain-text email body  
✅ Detect and validate global-format phone numbers  
✅ Use `spaCy` NER to extract locations (cities, countries)  
✅ Export clean structured data into `.csv`  

---

## 🔄 Workflow

```mermaid
graph TD;
  A[.eml Email Files] --> B[Parse Metadata (From, To, Subject, Date)];
  B --> C[Extract Body Text];
  C --> D[Find Phone Numbers (Regex + phonenumbers)];
  C --> E[Identify Locations (spaCy NER)];
  D --> F[Structured Python Dict];
  E --> F;
  F --> G[Export to CSV];
