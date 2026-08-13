![AI Resume Screener Banner](./Banner.jpeg)
AI Resume Screener

An AI-powered recruitment automation workflow that automates the initial resume screening process by comparing candidate resumes with job-specific requirements and generating a structured AI evaluation.
Built with n8n, Google Gemini, Google Sheets, Google Drive, ConvertAPI, and Gmail.

Overview:

AI Resume Screener streamlines the initial stage of candidate screening.

Candidates submit their information, resume, and desired job role through an n8n form. The workflow extracts the resume text, retrieves the relevant job requirements, and uses Google Gemini to evaluate the candidate against the selected position.

The system generates a match score, identifies relevant skills and experience, provides strengths and weaknesses, and produces a shortlist or reject decision. The results are then stored in Google Sheets and an automated email is sent to the candidate.

Key Features:

* Automated resume collection through n8n
* PDF resume text extraction using ConvertAPI
* Job-specific resume evaluation
* AI-powered analysis using Google Gemini
* Candidate match score from 0–100
* Skills and experience analysis
* Strengths and weaknesses identification
* Automated shortlist/reject decision
* Results stored in Google Sheets
* Automated candidate email notifications
* Support for multiple job roles

Workflow:

Candidate Submission
        ↓
    n8n Form
        ↓
    Resume PDF
        ↓
  PDF → Text
   ConvertAPI
        ↓
Job Requirements
 Google Sheets
        ↓
 Google Gemini
  AI Evaluation
        ↓
Match Score + Analysis
        ↓
Shortlist / Reject
      ↙     ↘
Google Sheets  Gmail

AI Evaluation:

The system generates a structured evaluation containing:

Field	Description
Candidate Name	Candidate name
Job Title	Selected position
Match Score	Resume-to-job match score
Skills Found	Relevant skills identified
Experience Summary	Relevant experience
Strengths	Strong matching areas
Weaknesses	Missing or weaker requirements
Decision	Shortlist or Reject
Reason	Explanation for the decision

Tech Stack:

Technology	Purpose
n8n	Workflow automation
Google Gemini	AI resume evaluation
Google Sheets	Job requirements and results
Google Drive	Resume handling
ConvertAPI	PDF-to-text conversion
Gmail	Automated communication
JavaScript / JSON	Data processing

Supported Job Roles:

The workflow can be configured for multiple positions, such as:

* AI Automation Intern
* Python Developer
* Data Analyst
* Frontend Developer

New roles can be added by updating the job requirements in Google Sheets.

n8n Workflow:

![AI Resume Screener Workflow](./Workflow-overview.png)

Setup:

1. Import the workflow JSON into n8n.
2. Configure the required credentials and API integrations.
3. Add job descriptions and requirements to Google Sheets.
4. Configure Google Drive and Gmail.
5. Activate the workflow and submit a test resume.

Future Improvements:

* Recruiter dashboard
* Batch resume processing
* Candidate ranking
* Screening analytics
* Human-in-the-loop approval
* Interview scheduling automation

Skills Demonstrated:

AI Automation · n8n · Prompt Engineering · Google Gemini · REST APIs · JSON · JavaScript · Google Sheets Automation · Google Drive Integration · PDF Processing · Conditional Logic · Automated Email Workflows

Project Summary:

AI Resume Screener is an end-to-end recruitment automation solution that transforms a candidate’s resume into a structured AI evaluation and automated screening decision.






