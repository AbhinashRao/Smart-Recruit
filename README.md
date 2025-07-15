# Smart-Recruit

End-to-End Resume Screening Automation with AI & n8n

> “In hiring, time is everything. But sifting through hundreds of resumes shouldn’t consume all of it.”

Smart Recruit is an AI-powered, fully automated recruitment assistant that reads, parses, evaluates, and logs resumes against job descriptions using n8n, Gemini AI, and the Google ecosystem — no manual work required.

---

## 🎯 Project Goal: Screen Smarter, Not Harder

Instead of building just another ATS, Smart Recruit aims to:

- 📬 Read resumes directly from Gmail
- 📤 Upload & organize them in Google Drive
- 📄 Extract structured content from PDFs (Resume + JD)
- 📌 Match resumes with job descriptions
- 🧠 Use Gemini AI to assess candidate fit and recommend action
- 📊 Update a centralized Google Sheet with results

---

## ⚙️ Workflow Architecture

This solution is built with **n8n**, leveraging multiple services:

### 1. **Gmail Trigger** — Resume Intake  
Listens for new resumes (PDFs) in a specific inbox like `jobs@company.com`.

### 2. **Google Drive Integration** — File Archiving  
Resumes are auto-uploaded to Drive and organized by job ID or candidate.

### 3. **PDF Parser** — Text Extraction  
- Parses Resume PDFs  
- Parses pre-uploaded Job Descriptions  
- Cleans and converts to structured text

### 4. **Metadata Association**  
A `Set` node allows recruiters to tag resumes with job IDs, sources, or other metadata.

### 5. **Gemini AI — Candidate Fit Evaluation**  
Structured prompt sent to Gemini AI:
### 6. **Structured Output Parser**  
Ensures AI response is converted into clean, machine-readable JSON.

### 7. **Information Extractor**  
Extracts:
- Name
- Email
- Phone
- Skills
- Education
- Years of Experience

### 8. **Google Sheets API — Data Logging**  
Appends all structured info to a shared sheet:
| Name   | Email    | Fit Score | Recommendation           | Skills              |
|--------|----------|-----------|---------------------------|---------------------|
| A. Rao | a@x.com  | 8/10      | Proceed to Tech Interview | Python, ML, APIs    |

---

## 🧰 Tech Stack

| Tool / API           | Purpose                                |
|----------------------|----------------------------------------|
| n8n                  | Workflow orchestration                 |
| Gmail API            | Resume intake                         |
| Google Drive API     | Resume + JD storage                   |
| PDF Parser (n8n)     | Text extraction from resumes/JDs      |
| Gemini AI            | Candidate fit evaluation              |
| Structured Parser    | Clean and readable AI output          |
| Information Extractor| Candidate detail parsing              |
| Google Sheets API    | Final data logging & recruiter view   |

---

## 🧠 Why It Matters

Recruiters waste hours screening resumes manually. With **Smart Recruit**:

✅ Screening becomes instant  
✅ Bias is minimized  
✅ Evaluation is consistent  
✅ All data is searchable and shareable

---

## 🌟 Final Thoughts

In the age of AI and automation, resume screening shouldn't be a manual chore.  
**Smart Recruit** transforms hours of recruiter busywork into minutes of AI-powered insight — letting teams focus on hiring the right people, faster.

---

## 📌 Author

**Madikonda Abhinash Rao**  
[LinkedIn](https://linkedin.com/in/abhinashrao) | [Email](mailto:abhinashrao28@gmail.com)

---
