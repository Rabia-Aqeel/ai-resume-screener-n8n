![AI Resume Screener Banner](./Banner.jpeg)
AI Resume Screener

An AI-powered recruitment automation workflow that automatically analyzes candidate resumes against job-specific requirements, generates a structured evaluation, and helps recruiters make faster initial screening decisions.

Built with: n8n, Google Gemini, Google Sheets, Google Drive, ConvertAPI, and Gmail.

Overview

AI Resume Screener automates the initial stage of the recruitment process.

Instead of manually reviewing every resume, recruiters can collect candidate information through an n8n form and let the workflow automatically process the resume, compare it with the selected job requirements, generate an AI-based evaluation, and store the final screening result.

Workflow

┌──────────────────────┐
│      Candidate       │
│  Resume + Job Role   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│      n8n Form        │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│     Google Drive     │
│    Resume Storage    │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│      ConvertAPI      │
│    PDF → Text        │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐       ┌──────────────────────┐
│  Resume Information  │◄──────│  Job Requirements    │
└──────────┬───────────┘       │   Google Sheets      │
           │                   └──────────────────────┘
           ▼
┌──────────────────────┐
│    Google Gemini     │
│   AI Evaluation      │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Structured Evaluation│
│ Match Score + Reason │
└──────────┬───────────┘
           │
           ▼
      ┌────┴────┐
      │ Decision│
      └────┬────┘
           │
     ┌─────┴─────┐
     ▼           ▼
┌──────────┐ ┌──────────┐
│ Shortlist│ │  Reject  │
└────┬─────┘ └────┬─────┘
     │            │
     └──────┬─────┘
            ▼
┌──────────────────────┐
│     Google Sheets    │
│   Screening Results  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│        Gmail         │
│ Automated Email      │
└──────────────────────┘


Key Features

* Automated candidate and resume collection through an n8n form
* PDF resume text extraction
* Job-specific resume evaluation
* AI-powered candidate analysis using Google Gemini
* Candidate match score from 0 to 100
* Relevant skills and experience analysis
* Strengths and weaknesses identification
* Automated shortlist or reject decision
* Screening results stored in Google Sheets
* Automated candidate email notifications
* Support for multiple job roles


AI Evaluation

For each candidate, the system generates a structured evaluation containing:

Field	Description
Candidate Name	Candidate name identified from the resume
Job Title	Selected position
Match Score	Overall resume-to-job match from 0 to 100
Skills Found	Relevant skills identified in the resume
Experience Summary	Summary of relevant experience
Strengths	Areas where the candidate matches well
Weaknesses	Missing or weaker requirements
Decision	Shortlist or Reject
Reason	Explanation supporting the decision


Tech Stack

Technology	Purpose
n8n	Workflow automation and orchestration
Google Gemini	AI-powered resume evaluation
Google Sheets	Job requirements and screening results
Google Drive	Resume file management
ConvertAPI	PDF-to-text conversion
Gmail	Automated candidate communication
JavaScript	Data processing and workflow logic
JSON	Structured data exchange

Workflow Components

The workflow consists of the following major stages:

1. Candidate submits their information and resume.
2. The selected job role is identified.
3. Job requirements are retrieved from Google Sheets.
4. The uploaded PDF is processed and converted into text.
5. Resume content and job requirements are provided to Google Gemini.
6. The AI generates a structured candidate evaluation.
7. The candidate receives a match score and screening decision.
8. The result is stored in Google Sheets.
9. An automated email is sent based on the decision.


Supported Job Roles

The workflow can be configured for different positions, including:

* AI Automation Intern
* Python Developer
* Data Analyst
* Frontend Developer

Additional positions can be added by updating the job requirements in Google Sheets.


Project Screenshots

n8n Workflow

Add your n8n workflow screenshot here.

Screening Results

Add your Google Sheets screening results screenshot here.

⸻

Setup

1. Import the workflow JSON into n8n.
2. Configure the required Google, Gemini, ConvertAPI, and Gmail credentials.
3. Create the required Google Sheets structure.
4. Add job descriptions and requirements to the Job Descriptions sheet.
5. Configure Google Drive for resume handling.
6. Activate the workflow.
7. Submit a test resume through the form.

⸻

Security and Privacy

This project is designed for initial candidate screening and should not replace final human hiring decisions.

For production deployment, appropriate measures should be implemented for protecting candidate information, managing API credentials, controlling access, and defining data-retention policies.

⸻

Future Improvements

* Recruiter dashboard
* Batch resume processing
* Candidate ranking
* Screening analytics
* Human-in-the-loop approval
* Interview scheduling automation
* Candidate database integration

⸻

Skills Demonstrated

AI Automation, n8n Workflow Automation, Prompt Engineering, Google Gemini, REST APIs, JSON, JavaScript, Google Sheets Automation, Google Drive Integration, PDF Processing, Conditional Logic, and Automated Email Workflows.

⸻

Project Summary

AI Resume Screener is an end-to-end recruitment automation workflow that transforms a candidate’s resume into a structured AI evaluation and automated screening decision.

Resume
   │
   ▼
Text Extraction
   │
   ▼
Job Requirement Matching
   │
   ▼
AI Evaluation
   │
   ▼
Match Score
   │
   ▼
Screening Decision
   │
   ▼
Automated Communication
   │
   ▼
Result Storage


![AI Resume Screener Workflow](./Workflow-overview.png)



