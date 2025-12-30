# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## IMPORTANT: Standard Email for Applications

**Always use `harsha.yellela@gmail.com` for all job applications** (not harsha7663@gmail.com which is the LinkedIn account email).

---

## IMPORTANT: On New Chat Session

**When opening this project in a new chat, Claude MUST:**

1. **Read this file first** (`CLAUDE.md`) to understand the project structure and instructions
2. **Check the Task Log** (at the bottom of this file) to see what was done in previous sessions
3. **Greet the user** with a brief status: what files exist and where things left off
4. **After completing any task**, update the Task Log section at the bottom of this file

### Example Greeting for New Chat:
```
Welcome back! I've read the project context.

Current status:
- Projects documented: [X] in projects.md
- Last task: [Description from Task Log]
- Ready for: [Next logical step or awaiting instructions]

How can I help you today?
```

---

## Repository Overview

This is a personal resume repository for Harsha Vardhan Yellela. It contains a single-page HTML resume, PDF exports, and context files for intelligent resume tailoring.

## File Structure

- `resume.html` - Main resume document (self-contained HTML with embedded CSS)
- `*.pdf` - PDF exports for different purposes (e.g., MLE/SDE roles, specific companies)
- `personal_details.md` - Personal information, education, work experience, and skills
- `projects.md` - Detailed project repository with skills mapping for resume tailoring

---

## Adding a New Project

When the user provides a new project, add it to `projects.md` following this structure:

```markdown
## Project N: [Project Name]

### Overview
- **Project Name:** [Full name with subtitle if applicable]
- **Role:** [Your role in the project]
- **Duration:** [Month Year – Month Year or "Present"]
- **Live URL:** [If applicable]
- **GitHub:** [If applicable]
- **Status:** [Active/Completed]

### Tech Stack
- **Category:** Technology1, Technology2
- [Add relevant categories: Backend, Frontend, Database, AI/ML, Cloud, DevOps, etc.]

### Key Features & Accomplishments
- [Bullet points with quantifiable achievements where possible]
- [Use action verbs: Built, Designed, Implemented, Reduced, Achieved, etc.]

### Skills Demonstrated
- [List of skills this project demonstrates]

### Best For Roles
- [List job titles this project is most relevant for]
```

After adding the project:
1. Update the "Skills to Projects Mapping" table
2. Update the "Notes for Resume Tailoring" section if needed
3. Update the "Last Updated" date

---

## Creating a Tailored Resume from Job Description

When the user provides a job description (JD), follow these steps:

### Step 1: Analyze the Job Description
- Extract key skills, technologies, and requirements
- Identify the role type (Backend, ML, Full Stack, Data Science, etc.)
- Note any specific keywords or phrases to incorporate

### Step 2: Read Context Files
- Read `personal_details.md` for personal info, education, experience, and skills
- Read `projects.md` for available projects

### Step 3: Select Relevant Projects
- Match projects from `projects.md` based on:
  - Tech stack alignment with JD requirements
  - Skills demonstrated that match JD
  - "Best For Roles" section guidance
- Select 2-4 most relevant projects (prioritize quality over quantity)
- Consider the "Skills to Projects Mapping" table for quick reference

### Step 4: Tailor the Resume
- Modify the Summary section to align with the target role
- Reorder/prioritize skills based on JD requirements
- Include selected projects with bullet points emphasizing JD-relevant accomplishments
- Adjust work experience bullet points to highlight relevant responsibilities
- Ensure keywords from JD appear naturally in the resume

### Step 5: Generate Output
- Update `resume.html` with tailored content
- Maintain existing CSS and formatting
- Keep resume to 1-2 pages (use page breaks appropriately)
- Inform user to generate PDF via browser print

### Quick Role-to-Project Reference
| Target Role | Priority Projects |
|-------------|-------------------|
| Backend/SDE | Job Portal, FieldFuze Backend (Go), Resumade, Lambda Microservices |
| API Developer | Job Portal (HATEOAS), FieldFuze Backend |
| DevOps/Platform | Telegram Toxicity (K8s), Online Learning Portal (Jenkins), ML Sentiment Loop |
| SRE | Telegram Toxicity (circuit breaker, monitoring), ML Sentiment Loop |
| ML/AI Engineer | Resume Optimizer (QLoRA), ML Sentiment Loop (MLOps), Sentiment Forecasting, Pneumonia Detection, Traffic Flow GNN, Food Classifier (EA-HPO) |
| LLM/NLP Engineer | Resume Optimizer, CRE Agent (RAG), ATS Matching |
| MLOps Engineer | ML Sentiment Loop (8 microservices), Telegram Toxicity |
| Cloud Engineer | Lambda Microservices (94 functions), ML Sentiment Loop, FieldFuze Backend |
| Full Stack | FieldFuze (Go + React Native), Job Portal, Resumade |
| Mobile Developer | FieldFuze Mobile (React Native, 104+ components) |
| Frontend | VSCode Portfolio (Next.js), FieldFuze Mobile |
| Data Scientist | Sentiment Forecasting, NLP Course, Food Classifier |
| Integration Engineer | Lambda Microservices (Stripe, Twilio, DocuSign, QuickBooks) |
| Automation Engineer | N8N, AgenticAI, ATS Matching |

---

## Working with the Resume

### Editing
The resume is a single HTML file with all styling inline in a `<style>` block. No build tools or dependencies are required.

### Generating PDFs
Open `resume.html` in a browser and use the browser's Print to PDF feature. The CSS includes print-specific styles (`@media print`) for proper rendering.

### Key CSS Considerations
- Uses `page-break-inside: avoid` to keep entries together when printing
- `page-break-before: always` is used to force page breaks between sections
- Table-layout CSS is used for header/subheader alignment (left content, right dates)
- User-select properties are carefully set to allow text copying while excluding bullet markers

---

## LinkedIn Resume Selection (For Job Applications)

When applying to jobs on LinkedIn using Easy Apply, select the appropriate resume based on the role type:

| Role Type | Resume to Use | File Name |
|-----------|---------------|-----------|
| **Software Engineer / SDE / Backend / Full Stack** | SDE Resume | `Harsha_Yellela_SDE.pdf` |
| **ML Engineer / AI Engineer / Data Scientist / NLP / CV** | ML-Engineer Resume | `Harsha_Yellela_ML-Engineer.pdf` |
| **DevOps / Platform / SRE / Cloud Engineer** | DevOps Resume | `Harsha_Yellela_DevOps.pdf` |
| **General / Mixed / Unclear roles** | Default Resume | `Harsha_Yellela_resume.pdf` |

### LinkedIn Resume Selection Tips:
1. **Check "Show more resumes"** - LinkedIn may hide some resumes under this dropdown
2. **Match keywords** - If job title contains "ML", "AI", "Data" → use ML resume; "DevOps", "Platform", "SRE" → use DevOps resume
3. **Default to SDE** for generic "Software Engineer" roles (not the general resume)
4. **Speech/NLP/CV roles** count as ML/AI even if titled differently

### Available Resumes on LinkedIn:
- `Harsha_Yellela_resume.pdf` (274 KB) - General portfolio
- `Harsha_Yellela_SDE.pdf` (221 KB) - Software Development Engineer focused
- `Harsha_Yellela_ML-Engineer.pdf` (227 KB) - Machine Learning focused
- `Harsha_Yellela_DevOps.pdf` (272 KB) - DevOps/Platform focused

---

## Job Application Tracking

**IMPORTANT:** After successfully submitting ANY job application (Indeed, LinkedIn, or any other platform), Claude MUST update the job applications CSV file.

### CSV File Location
`/Users/HAR5HA/Desktop/resume/job_applications.csv`

### CSV Format
```csv
Job Number,Position,Company,Location,Status,Date Applied
```

### After Each Successful Application:
1. **Read the current CSV** to get the last job number
2. **Append a new row** with:
   - `Job Number`: Increment from last entry
   - `Position`: Job title
   - `Company`: Company name
   - `Location`: Remote/City/State
   - `Status`: "Applied"
   - `Date Applied`: Current date (YYYY-MM-DD format)

### Example Entry:
```csv
11,Software Engineer,Google,Remote - Mountain View CA,Applied,2025-12-29
```

### Notes:
- Update the CSV immediately after seeing "Your application has been submitted" confirmation
- Include location details when available (Remote, City, State)
- Keep position titles concise but accurate
- This tracking helps maintain a record of all applications across sessions

---

## IMPORTANT: Job Application Permissions (Pre-Authorized Actions)

**The user has granted FULL PERMISSION for the following actions during job applications. Do NOT ask for confirmation - just proceed:**

### Pre-Authorized Actions:
1. **Fill all application form fields** using data from `JOB_APPLICATION_CONTEXT.md` and `personal_details.md`
2. **Sign eSignatures** - Enter full name "Harsha Vardhan Yellela" and email "harsha.yellela@gmail.com" on authorization forms
3. **Accept background check authorizations** - Reference checks, criminal background checks, employment verification
4. **Accept terms and agreements** - Privacy policies, application terms, cookie policies for job portals
5. **Submit applications** - Click submit/apply buttons without asking for final confirmation
6. **Select demographic information** - Gender: Male, Ethnicity: Asian, Veteran: No, Disability: No
7. **Choose salary ranges** - Use $100,000-$110,000 or midpoint of posted range
8. **Login via LinkedIn/OAuth** - When LinkedIn login is available, use it to pre-fill data

### Standard Job Application Workflow (No Questions Needed):
1. Navigate to job posting URL
2. Click "Apply" button
3. Login via LinkedIn if available (user will handle password if needed)
4. Upload appropriate resume based on role type (ML/SDE/DevOps)
5. Fill all form fields using context files
6. Sign any eSignature/authorization sections
7. Review and submit
8. Update `job_applications.csv` with new entry
9. Confirm submission to user

### What Still Requires User Action:
- **Password entry** - Claude cannot enter passwords; user must do this
- **File selection dialogs** - Native OS file pickers require user interaction
- **CAPTCHA/bot detection** - User must complete these manually
- **Two-factor authentication** - User must handle 2FA codes

### Resume Selection by Role Type:
| Role Keywords | Resume File |
|---------------|-------------|
| ML, AI, Data Science, NLP, CV, Deep Learning | `Harsha_Yellela_ML-Engineer.pdf` |
| SDE, Software Engineer, Backend, Full Stack | `Harsha_Yellela_SDE.pdf` |
| DevOps, Platform, SRE, Cloud, Infrastructure | `Harsha_Yellela_DevOps.pdf` |
| General/Unclear | `Harsha_Yellela_resume.pdf` |

### Key Form Field Values (Quick Reference):
| Field | Value |
|-------|-------|
| Full Name | Harsha Vardhan Yellela |
| Email | harsha.yellela@gmail.com |
| Phone | 248-497-9965 or +1-248-497-9965 |
| Location | Southfield, MI, USA |
| Work Authorization | Yes (F-1 OPT) |
| Sponsorship Needed | Yes (H-1B) |
| Willing to Relocate | Yes |
| Salary Range | $100,000 - $110,000 (negotiable) |
| Start Date | Immediate / 2 weeks |
| Current Supervisor | Professor Paula Lauren (for GRA role) |

---

## Cover Letter Handling (Optional Fields)

When a job application has an **optional** cover letter upload field:

### Decision Matrix:
| Scenario | Action |
|----------|--------|
| **High-value role** (Big 4, FAANG, Senior positions) | Generate tailored cover letter |
| **Role with specific requirements** matching Harsha's skills | Generate cover letter |
| **Standard Easy Apply** with many applicants | Skip (unless user requests) |
| **User explicitly requests** | Always generate |

### Cover Letter Generation Process:
1. **Create folder** (if not exists): `temp_cvr_ltrs/`
2. **File naming**: `{Company}_{Role}_Cover_Letter.txt`
   - Example: `EY_MLE_Cover_Letter.txt`
3. **Tailor content** to match:
   - Job requirements from posting
   - Harsha's relevant experience from `JOB_APPLICATION_CONTEXT.md`
   - Specific technologies mentioned in JD
4. **Format**: Plain text, professional business letter format
5. **Inform user** of file location so they can upload manually if needed

### Cover Letter Template Structure:
```
V Harsha Vardhan Yellela
Ferndale, MI 48220
harsha.yellela@gmail.com | (248) 497-9965
LinkedIn: linkedin.com/in/har5ha-7663 | GitHub: github.com/HAR5HA-7663

[Date]

[Company Name]
[Department/Team]

Dear Hiring Manager,

[Opening - Express interest, mention specific role]

[Body 1 - Current role highlights matching JD requirements]

[Body 2 - Technical skills alignment with bullet points]

[Body 3 - Previous experience relevance]

[Closing - Express enthusiasm, availability]

Sincerely,
V Harsha Vardhan Yellela
```

### Key Points to Highlight (by role type):
| Role Type | Cover Letter Focus |
|-----------|-------------------|
| **ML/AI Engineer** | LangChain, CrewAI, RAG systems, QLoRA fine-tuning, MLOps pipelines |
| **Backend/SDE** | FastAPI, Go, AWS Lambda, microservices, enterprise clients (Ferrari, Boeing) |
| **DevOps/Platform** | Kubernetes, EKS, Jenkins CI/CD, Terraform, monitoring (Prometheus/Grafana) |
| **Cloud Engineer** | AWS services, serverless (94 Lambda functions), IaC, SageMaker |

### Cleanup:
- Cover letters in `temp_cvr_ltrs/` are temporary
- User can delete after application is submitted
- Do NOT commit cover letters to git (add to .gitignore if needed)

---

## Resume Tailoring Hacks (Optimization Insights)

**Key patterns for faster, better resume generation:**

1. **ML Engineer Resume Formula:**
   - Summary: Lead with "Machine Learning Engineer" + LLM fine-tuning + deep learning architectures + MLOps
   - Skills order: ML Frameworks → Deep Learning → LLM/Fine-tuning → NLP → CV → MLOps → Languages
   - Top projects: QLoRA fine-tuning > MLOps pipeline > LSTM/time-series > CV/medical > GNN (unique differentiator)

2. **Project Selection Priority:**
   - Always include 1 LLM/fine-tuning project (shows modern ML skills)
   - Always include 1 MLOps project (shows production-readiness)
   - Include 1-2 domain-specific (CV, NLP, GNN based on JD)
   - Include 1 unique/differentiating project (GNN, Robotics, etc.)

3. **Bullet Point Formula:**
   - Format: `[Action verb] + [specific tech] + [quantifiable result]`
   - Example: "Fine-tuned Qwen3-4B using QLoRA (4-bit NF4), reducing GPU memory to 18-22GB"
   - Always bold key technologies and metrics

4. **Page Break Strategy:**
   - Page 1: Summary, Experience, Skills, 3 projects
   - Page 2: 2-3 more projects, Education, Achievements
   - Use `<div style="page-break-before: always;"></div>` before 4th project

5. **Skills Section Optimization:**
   - Group by category, not alphabetically
   - Put JD-matching skills first in each category
   - Combine related items with "|" separator to save space

---

## Task Log

**Instructions for Claude:** After completing any significant task, add an entry here with the date and description. Keep entries concise. **Only keep the last 4 entries** - delete older ones when adding new. This helps future chat sessions understand the project state.

### Log Entries

| Date | Task Completed | Details |
|------|----------------|---------|
| 2025-12-29 | LinkedIn ML batch | Applied to 15+ ML Engineer jobs via LinkedIn (Databricks, Pinterest, Cisco, Moveworks, AAA Life, etc.) |
| 2025-12-29 | MigrateMate ML batch | Applied to 10 ML jobs from MigrateMate including Lucid Motors, Snap Inc., EY (with cover letter) |
| 2025-12-29 | EY application | Completed full EY ML Engineer Senior application with tailored cover letter saved to `temp_cvr_ltrs/` |
| 2025-12-29 | Cover letter docs | Added "Cover Letter Handling" section to CLAUDE.md with decision matrix, template, and process |

### Pending/In Progress
- Ready for new applications
- Total applications: 77 (CSV job_applications.csv)

### Current State Summary
- **Projects in projects.md:** 27 total
  - ML/AI (10): Resume Optimizer, Sentiment Forecasting, Pneumonia Detection, Food Classifier, ATS Matching, NLP Course, Air Quality, Hybrid CMA-ES, Traffic Flow GNN, Stretch2
  - Backend (5): Job Portal, FieldFuze Backend, Resumade, Lambda Microservices, AviationStack
  - MLOps/Platform (4): ML Sentiment Loop, Telegram Toxicity, Online Learning Portal, AWS ML Projects
  - Full Stack (3): FieldFuze, Resumade, Car Dealer App
  - AI Agents/RAG (3): AgenticAI, CRE Agent, N8N
  - Mobile/IoT (3): FieldFuze Mobile, DOMUS, Covid-analyzer
  - Frontend (1): VSCode Portfolio
  - Robotics (1): Stretch2 Robot
- **personal_details.md:** Complete with 17+ skill categories (added ROS, IoT, GNN, Embedded)
- **resume.html:** Contains current resume (can be tailored per JD)

---

*End of CLAUDE.md*
