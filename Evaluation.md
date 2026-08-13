# Evaluation & Testing

## Overview

The AI Resume Screener was tested using real screening workflow runs to evaluate its ability to analyze resumes against job requirements and automatically generate candidate screening decisions.

The system processes a submitted resume, extracts the resume content, compares it with the relevant job description using AI, generates a match score and screening analysis, stores the result in Google Sheets, and triggers an automated email based on the final decision.

---

## Test Dataset

| Metric | Result |
|---|---:|
| Resumes Tested | 29 |
| Job Roles Tested | 4 |
| Shortlisted | 14 |
| Rejected | 14 |
| Human Review | 1 |

The screening results are stored in the accompanying Excel file:

Screening-results.xlsx

---

## Testing Workflow

Each test followed the same automated pipeline:

1. A candidate submits their resume through the application form.
2. The selected job role is identified.
3. The corresponding job description is retrieved.
4. The uploaded PDF resume is processed and converted into text.
5. The AI analyzes the resume against the job requirements.
6. The system generates:
   - Overall match score
   - Technical skills
   - Experience analysis
   - Projects
   - Certifications
   - Strengths
   - Weaknesses
   - Missing skills
   - Screening decision
   - Scoring rationale
7. The screening result is saved to Google Sheets.
8. The decision logic determines the next action.
9. An automated email notification is sent based on the screening outcome.

---

## Screening Results

The system generated three possible outcomes:

### Shortlisted

Candidates whose resumes demonstrated a strong match with the requirements were marked as:

`Shortlisted`

### Rejected

Candidates with insufficient alignment with the job requirements were marked as:

`Rejected`

### Human Review

Cases requiring additional human assessment were marked as:

`Human Review`

This provides a safer alternative to forcing every candidate into an automatic accept/reject decision.

---

## Results Summary

The 29 test runs produced the following results:

- **14 candidates — Shortlisted**
- **14 candidates — Rejected**
- **1 candidate — Human Review**

The complete screening results are available in the accompanying Excel dataset.

---

## What Was Evaluated

The testing focused on whether the automation could successfully:

- Process submitted resume documents
- Extract relevant resume information
- Match candidates against the appropriate job description
- Identify relevant technical skills
- Evaluate experience and projects
- Identify strengths and missing skills
- Generate a numerical match score
- Produce a screening decision
- Store structured results in Google Sheets
- Trigger automated email notifications

---

## Evaluation Metrics

Accuracy, Precision, Recall, and F1-score are not reported in this evaluation because these metrics require independently verified ground-truth labels for each candidate.

The current evaluation therefore focuses on **workflow execution and screening-output validation** rather than claiming model classification accuracy.

If human-verified labels are established for the test dataset in the future, standard classification metrics can be calculated.

---

## Data Privacy

Candidate information used for the public GitHub version is anonymized.

Personally identifiable information such as names, email addresses, phone numbers, and other sensitive candidate information should not be exposed in the public repository.

The published evaluation data is intended only to demonstrate the functionality and testing of the AI Resume Screener.

---

## Limitations

The screening decision is AI-assisted and should not be treated as a replacement for human recruitment judgment.

Potential sources of variation include:

- Resume formatting and quality
- Different ways candidates describe similar skills
- Ambiguous job requirements
- AI interpretation of experience and qualifications
- Missing information in resumes

For this reason, the workflow includes a **Human Review** outcome for cases that may require additional assessment.

---

## Conclusion

The AI Resume Screener successfully completed 29 end-to-end screening tests across 4 job roles.

The testing demonstrates that the workflow can automate the complete screening pipeline from resume submission and AI analysis to structured result storage and automated email notification.

The evaluation dataset and workflow configuration are included in this repository to provide reproducible evidence of the project implementation.
