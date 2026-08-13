![AI Resume Screener Banner](./Banner.jpeg)

AI Resume Screener

An AI-powered resume screening and candidate evaluation workflow built with n8n, Google Gemini, Google Sheets, and Gmail. The system automates the initial recruitment screening process by collecting applications, extracting resume data, comparing candidates against job requirements, generating an AI-based evaluation, and delivering structured results to HR.

Overview

The AI Resume Screener is designed to reduce the manual effort involved in reviewing resumes during the initial hiring stage.

Candidates submit their personal information, select a job role, and upload their resume in PDF format. The workflow then retrieves the relevant job description, extracts the resume text, evaluates the candidate using Google Gemini, assigns a weighted score, generates a hiring recommendation, and stores the results in Google Sheets.

The workflow supports roles such as AI Automation Intern, Python Developer, Data Analyst, and Frontend Developer.

Key Features

* Candidate application form with PDF resume upload
* Input validation and application ID generation
* Automatic job description matching from Google Sheets
* PDF resume text extraction
* AI-powered candidate evaluation using Google Gemini
* Weighted scoring across technical skills, experience, education, projects, certifications, and overall fit
* Automatic hiring decision:
    * 70+ — Shortlisted
    * 50–69 — Human Review
    * Below 50 — Rejected
* Candidate strengths, weaknesses, and missing skills analysis
* Candidate-specific interview questions
* AI-generated screening summary and scoring rationale
* Structured screening results stored in Google Sheets
* HR notification through Gmail
* Candidate application acknowledgement email

The workflow’s AI evaluation is configured to assess six categories and apply weighted scoring to produce the overall candidate score.

Workflow

Candidate Application
        ↓
Validate & Normalize Input
        ↓
Fetch Job Description
        ↓
Match Selected Job Role
        ↓
Prepare Resume PDF
        ↓
Extract Resume Text
        ↓
Merge Resume + Job Data
        ↓
AI Resume Screening with Gemini
        ↓
Parse & Validate AI Response
        ↓
Save Screening Results
        ↓
 ┌───────────────────────┐
 ↓                       ↓
HR Email            Candidate Email

The workflow connections follow this end-to-end sequence, with the final screening results branching into HR and candidate email notifications.

AI Evaluation

For each candidate, Gemini evaluates:

* Technical Skills
* Experience
* Education
* Projects
* Certifications
* Overall Fit

The system also generates:

* Overall score
* Hiring verdict
* Strengths
* Weaknesses
* Missing skills
* AI summary
* Five interview questions
* Scoring rationale

The AI response is parsed and validated before the results are saved, with an additional safeguard that enforces the final verdict according to the configured score thresholds.

Data Storage

Screening results are automatically appended to a Google Sheets spreadsheet containing candidate information, job details, scores, verdict, strengths, weaknesses, missing skills, interview questions, AI summary, and scoring rationale.

Technologies Used

* n8n
* Google Gemini API
* Google Sheets
* Gmail
* JavaScript
* PDF text extraction
* REST API / HTTP Request
* JSON

Project Structure

AI Resume Screener
├── Candidate Application Form
├── Input Validation
├── Job Description Matching
├── Resume PDF Processing
├── AI Candidate Evaluation
├── AI Response Validation
├── Google Sheets Storage
└── Email Notifications

Use Case

This workflow can be used by recruiters, HR teams, and organizations to automate the first stage of recruitment and quickly identify candidates who match specific job requirements.

It is designed as an automation workflow rather than a simple AI prompt, combining form handling, data processing, document extraction, job matching, AI evaluation, structured storage, and automated communication.

Setup

1. Import the workflow JSON into n8n.
2. Configure Google Sheets credentials and connect the required job description and screening results sheets.
3. Configure the Google Gemini API credentials.
4. Configure Gmail credentials for HR and candidate notifications.
5. Update the job descriptions and required skills in the Google Sheet.
6. Activate the workflow and test it with sample resumes.

Project Goal

The goal of this project is to demonstrate how AI and workflow automation can be combined to build a practical recruitment screening system that reduces repetitive manual work while providing structured and consistent candidate evaluations.
![AI Resume Screener Workflow](./Workflow-overview.png)



