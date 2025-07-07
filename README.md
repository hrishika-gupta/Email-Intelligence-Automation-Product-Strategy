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

1. 📂 Load `.eml` Email Files
     └─ Loop through directory of email files

2. 🧾 Parse Email Metadata
     └─ Extract Subject, From, To, Date

3. 📝 Extract Body Text
     └─ Decode plain text from multipart email structure

4. 📞 Detect Phone Numbers
     └─ Use regex + `phonenumbers` to validate

5. 🌍 Extract Locations
     └─ Use spaCy NER to find cities, countries (label = GPE)

6. 🧠 Structure into Dicts
     └─ Combine all extracted data per email

7. 📤 Export to CSV
     └─ Create `output.csv` with clean fields


<img width="966" alt="Screenshot 2025-07-07 at 4 50 45 PM" src="https://github.com/user-attachments/assets/b6d5bf29-f3be-4b75-84b3-f735e5cd9598" />


📈 Impact
✅ Reduced email review time from days to minutes
✅ Helped Afforest’s product team prioritize features based on actual customer interest
✅ Enabled Sales to qualify leads by geography and contactability
✅ Created a reusable framework for future contact parsing

🧠 Learnings
How to use Python for real-world automation tasks
Applied NLP for named entity extraction
Cleaned noisy, unstructured text data
Built production-style scripts from scratch for business teams



