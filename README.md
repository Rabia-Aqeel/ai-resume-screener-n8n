![AI Resume Screener Banner](./Banner.jpeg)
# AI Resume Screener

An AI-powered recruitment automation workflow that automates the initial resume screening process by comparing candidate resumes with job-specific requirements and generating a structured AI evaluation.

Built with **n8n, Google Gemini, Google Sheets, Google Drive, ConvertAPI, and Gmail**.

## Overview

AI Resume Screener streamlines the initial stage of candidate screening.

Candidates submit their information, resume, and desired job role through an n8n form. The workflow extracts the resume text, retrieves the relevant job requirements, and uses Google Gemini to evaluate the candidate against the selected position.

The system generates a match score, identifies relevant skills and experience, provides strengths and weaknesses, and produces a screening decision. The result is stored in Google Sheets and an automated email can be sent based on the outcome.

## Key Features

- Automated resume collection through n8n
- PDF resume text extraction using ConvertAPI
- Job-specific resume evaluation
- AI-powered analysis using Google Gemini
- Candidate match score from 0–100
- Skills and experience analysis
- Strengths and weaknesses identification
- Automated shortlist/reject decision
- Results stored in Google Sheets
- Automated candidate email notifications
- Support for multiple job roles

## Workflow

```text
Candidate Submission
        |
        v
    n8n Form
        |
        v
    Resume PDF
        |
        v
  PDF to Text
   ConvertAPI
        |
        v
Job Requirements
 Google Sheets
        |
        v
 Google Gemini
  AI Evaluation
        |
        v
Match Score + Analysis
        |
        v
   Screening Decision
      /      |       \
     v       v        v
Shortlist  Human     Reject
           Review
      \       |       /
       \      |      /
        v     v     v
        Google Sheets
             |
             v
            Gmail

## AI Evaluation

The system generates a structured evaluation containing:

| Field | Description |
|---|---|
| Candidate Name | Candidate name identified from the resume |
| Job Title | Selected position |
| Match Score | Resume-to-job match score from 0–100 |
| Skills Found | Relevant skills identified in the resume |
| Experience Summary | Summary of relevant experience |
| Strengths | Strong matching areas |
| Weaknesses | Missing or weaker requirements |
| Decision | Shortlist, Human Review, or Reject |
| Reason | Explanation supporting the decision |

## Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation and orchestration |
| Google Gemini | AI-powered resume evaluation |
| Google Sheets | Job requirements and screening results |
| Google Drive | Resume file handling |
| ConvertAPI | PDF-to-text conversion |
| Gmail | Automated candidate communication |
| JavaScript | Data processing and workflow logic |
| JSON | Structured data exchange |

## Supported Job Roles

The workflow can be configured for multiple positions, such as:

- AI Automation Intern
- Python Developer
- Data Analyst
- Frontend Developer

New roles can be added by updating the job requirements in Google Sheets.

## Project Screenshots

### n8n Workflow

_Add your n8n workflow screenshot here._

### Screening Results

_Add your Google Sheets results screenshot here._

## Setup

1. Import the workflow JSON into n8n.
2. Configure the required credentials and API integrations.
3. Add job descriptions and requirements to Google Sheets.
4. Configure Google Drive and Gmail.
5. Activate the workflow and submit a test resume.

## Security and Privacy

This project is designed to assist with initial candidate screening and should not replace final human hiring decisions.

For production deployment, appropriate measures should be implemented for protecting candidate information, managing API credentials, controlling access, and defining data-retention policies.

## Future Improvements

- Recruiter dashboard
- Batch resume processing
- Candidate ranking
- Screening analytics
- Human-in-the-loop approval
- Interview scheduling automation
- Candidate database integration

## Skills Demonstrated

**AI Automation · n8n · Prompt Engineering · Google Gemini · REST APIs · JSON · JavaScript · Google Sheets Automation · Google Drive Integration · PDF Processing · Conditional Logic · Automated Email Workflows**

## Project Summary

AI Resume Screener is an end-to-end recruitment automation solution that transforms a candidate's resume into a structured AI evaluation and automated screening decision.

![AI Resume Screener Workflow](./Workflow-overview.png)



