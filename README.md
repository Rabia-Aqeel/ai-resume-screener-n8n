![AI Resume Screener Banner](./Banner.jpeg)
🤖 AI Resume Screener

An end-to-end AI-powered recruitment automation workflow built with n8n and Google Gemini to automate resume screening, candidate evaluation, scoring, and hiring decisions.

1️⃣ 📌 Overview

AI Resume Screener is an AI-powered recruitment automation system designed to automate the initial candidate screening process.

The workflow receives a candidate’s information and resume PDF, extracts the resume content, retrieves the relevant job requirements, and uses an AI model to evaluate how well the candidate matches the position.

Instead of manually reviewing every resume, recruiters receive a structured candidate evaluation with a match score, skills analysis, strengths, weaknesses, and recommendation.

🎯 What it solves

Traditional resume screening can be:

* Time-consuming
* Repetitive
* Difficult to scale
* Inconsistent between candidates

This automation reduces manual screening effort by turning the process into a structured, AI-assisted workflow.


2️⃣ ⚙️ How It Works

The complete workflow follows this pipeline:

Candidate Submission → Resume Processing → Job Data Retrieval → AI Evaluation → Structured Output → Candidate Decision → Google Sheets → Email Notification

🔄 Workflow Steps

1. Candidate submits application
    * Full Name
    * Email
    * Phone
    * Resume PDF
    * Job Role
2. Resume processing
    * Resume PDF is received through the n8n form.
    * The PDF is converted into readable text using ConvertAPI.
3. Job requirement retrieval
    * The selected job role is matched with the corresponding job description.
    * Job requirements, required skills, experience and qualifications are retrieved from Google Sheets.
4. AI-powered evaluation
    * Resume content is compared against the selected job requirements.
    * Google Gemini evaluates the candidate.
5. Structured candidate analysis
    The AI generates:
    * Match Score
    * Skills Found
    * Experience Summary
    * Strengths
    * Weaknesses
    * Hiring Decision
    * Decision Reason
6. Candidate decision
    * The candidate is evaluated against the defined screening criteria.
    * The workflow determines whether the candidate should be Shortlisted or Rejected.
7. Result storage
    * Candidate evaluation results are automatically saved into Google Sheets.
8. Email notification
    * Candidates can receive an automated email based on the final screening decision.


3️⃣ 🧠 AI Evaluation

The AI evaluation is designed around the actual requirements of the selected job role rather than simply analyzing the resume in isolation.

Evaluation factors

Factor	Description
🎯 Match Score	Overall compatibility with the position
🛠️ Skills	Relevant skills identified from the resume
💼 Experience	Candidate’s relevant experience
💪 Strengths	Strong areas matching the job
⚠️ Weaknesses	Missing or weaker requirements
📊 Decision	Shortlist or Reject
📝 Reason	Explanation behind the decision

This makes the output more useful than a simple AI-generated resume summary.


4️⃣ 🏗️ Architecture

Candidate
    │
    ▼
n8n Form
    │
    ├── Candidate Information
    ├── Resume PDF
    └── Selected Job Role
            │
            ▼
     Google Sheets
     Job Descriptions
            │
            ▼
       Resume PDF
            │
            ▼
        ConvertAPI
            │
            ▼
       Resume Text
            │
            ▼
    Resume + Job Data
            │
            ▼
      Google Gemini
       AI Evaluation
            │
            ▼
   Structured Output Parser
            │
            ▼
        Code Node
      Validation/Parsing
            │
            ▼
        IF Decision
       ┌────┴────┐
       ▼         ▼
   Shortlist   Reject
       │         │
       └────┬────┘
            ▼
      Google Sheets
       Save Results
            │
            ▼
      Gmail Notification


5️⃣ 🧩 Tech Stack

Technology	Purpose
n8n	Workflow automation & orchestration
Google Gemini	AI-powered candidate evaluation
Google Sheets	Job data & evaluation result storage
Google Drive	Resume/file handling
ConvertAPI	PDF-to-text conversion
Gmail	Automated candidate communication
JavaScript	Data parsing and validation
JSON	Structured AI output


6️⃣ ✨ Key Features

* 🤖 AI-powered resume screening
* 📄 Automated PDF resume processing
* 🎯 Job-specific candidate evaluation
* 📊 Candidate match scoring
* 🧠 AI-generated strengths and weaknesses
* 🛠️ Skills extraction
* 💼 Experience analysis
* ✅ Automated shortlist/reject decision
* 📑 Structured evaluation output
* 📊 Google Sheets result management
* 📧 Automated email notifications
* 🔄 Fully automated n8n workflow


7️⃣ 📋 Example AI Output

{
  "candidateName": "Candidate Name",
  "jobTitle": "AI Automation Intern",
  "matchScore": 86,
  "skillsFound": [
    "n8n",
    "Python",
    "REST APIs",
    "Google Sheets",
    "AI Automation"
  ],
  "experienceSummary": "Relevant academic and project experience in AI automation and workflow development.",
  "strengths": [
    "Strong automation experience",
    "Relevant technical skills",
    "Good alignment with job requirements"
  ],
  "weaknesses": [
    "Limited professional experience"
  ],
  "decision": "Shortlist",
  "reason": "The candidate demonstrates strong alignment with the required skills and qualifications."
}

⸻

8️⃣ 📊 Result Management

All evaluated candidates are stored in Google Sheets, allowing recruiters to maintain a centralized screening record.

The result sheet can contain information such as:

* Candidate Name
* Email
* Phone
* Job Role
* Match Score
* Skills Found
* Experience Summary
* Strengths
* Weaknesses
* Decision
* Reason

This creates a simple searchable candidate evaluation database without requiring a separate recruitment platform.

⸻

9️⃣ 🔐 Reliability & Validation

The workflow includes processing and validation steps to make the AI-generated output more reliable.

The system:

* Parses the AI response
* Validates the returned structure
* Extracts required fields
* Handles structured JSON output
* Applies decision logic
* Stores the final result in a consistent format

This helps prevent malformed AI responses from directly entering the final candidate database.

⸻

🔟 🚀 Future Improvements

Possible extensions for a production-grade version include:

* 📈 Recruiter analytics dashboard
* 🧮 Automated screening performance metrics
* 🔍 Semantic skill matching
* 🗂️ Candidate database with search and filters
* 📧 Personalized recruiter summaries
* 🧠 Multi-model evaluation
* ⚖️ Bias and fairness monitoring
* 🔐 Secure candidate data handling
* 📊 Recruitment funnel analytics
* 👥 Human-in-the-loop recruiter approval

⸻

1️⃣1️⃣ 💡 Why This Project?

This project demonstrates how AI can be combined with workflow automation to solve a real-world business problem.

Instead of creating a simple AI chatbot, the system combines:

AI + Automation + APIs + Data Processing + Decision Logic + Business Workflow

The result is an end-to-end automated screening pipeline that can be adapted to different job roles and recruitment requirements.

⸻

1️⃣2️⃣ 📸 Workflow Preview

Add your n8n workflow screenshot here.

[ Add Workflow Screenshot ]

⸻

1️⃣3️⃣ 🗂️ Project Structure

AI-Resume-Screener/
│
├── README.md
├── workflow/
│   └── AI Resume Screener.json
│
├── screenshots/
│   ├── workflow.png
│   ├── candidate-form.png
│   └── evaluation-results.png
│
└── examples/
    └── sample-output.json

⸻

1️⃣4️⃣ 🎓 Skills Demonstrated

This project demonstrates practical experience with:

* AI Automation
* n8n Workflow Development
* Prompt Engineering
* LLM Integration
* Google Gemini API
* REST APIs
* JSON Data Processing
* JavaScript
* Google Sheets Automation
* Google Drive Integration
* PDF Processing
* Conditional Workflow Logic
* Structured AI Output
* End-to-End Workflow Design

⸻

1️⃣5️⃣ 📌 Conclusion

AI Resume Screener demonstrates how AI and automation can transform a repetitive recruitment task into a structured, scalable workflow.

The project combines n8n orchestration, AI-powered evaluation, document processing, structured outputs, business logic, data storage, and automated communication into a single end-to-end system.

Built with n8n + Google Gemini + APIs + Automation 🚀
![AI Resume Screener Workflow](./Workflow-overview.png)



