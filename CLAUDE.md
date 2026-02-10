# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## IMPORTANT: Standard Email for Applications

**Always use `harsha.yellela@gmail.com` for all job applications** (not harsha7663@gmail.com which is the LinkedIn account email).

---

## IMPORTANT: User Communication Preferences

**Writing Style for Emails/Messages:**
- **NEVER use markdown formatting** (no `**bold**`, `*italics*`, or bullet points) when composing emails or messages on behalf of the user
- Write in a **natural, conversational tone** - like a real person, not an AI
- Keep it professional but warm and authentic
- The user explicitly said: "you are writing it like a llm" and "those ** will surely let them know that" - meaning markdown symbols appearing literally in emails is a dead giveaway

**Work Style:**
- User types quickly with typos (e.g., "reaply", "sned", "prefrennces") - understand intent without asking for clarification
- User prefers **autonomous action** - don't ask unnecessary questions, just do the task
- When user says things like "i did it continue" - they've handled a small thing themselves, keep moving
- Be efficient and action-oriented

**Gmail Account:**
- `harsha.yellela@gmail.com` is Gmail account #4 (use `/u/4/` in URLs)
- This is the primary job application email

**Response Format:**
- Be concise, not verbose
- Use tables and structured summaries for status updates
- Don't over-explain or add unnecessary caveats

---

## IMPORTANT: temp.txt Queue System

**Purpose:** temp.txt is used for quick inter-session communication - a queue of length 5.

**How it works:**
- When you need to send text to the user or save notes between sessions, add to temp.txt
- Keep only the **5 most recent entries** - delete the oldest when adding new
- Each entry should have a header with date/time and purpose
- Format: `---\n[DATE] - [PURPOSE]\n[CONTENT]\n`

**Current queue structure:**
```
---
[Entry 1 - oldest, gets deleted when 6th entry is added]
---
[Entry 2]
---
[Entry 3]
---
[Entry 4]
---
[Entry 5 - newest]
```

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

```
D:\Desktop\resume\
├── CLAUDE.md                    # Project instructions (this file)
├── resumes/                     # All resume files
│   ├── resume.html              # Main resume (self-contained HTML)
│   ├── Harsha_Yellela_resume.pdf
│   ├── Harsha_Yellela_ML-Engineer.pdf
│   ├── Harsha_Yellela_SDE.pdf
│   └── Harsha_Yellela_DevOps.pdf
├── references/                  # Context files for tailoring
│   ├── personal_details.md      # Personal info, education, skills
│   ├── projects.md              # Project repository
│   ├── JOB_APPLICATION_CONTEXT.md
│   └── Build_Fellowship_QA.md
├── job_tracking/                # Application tracking
│   ├── job_applications.csv     # All applications log
│   └── referral_requests.csv    # Networking/referral tracking
├── ranked_jobs/                 # Company-specific job rankings
│   ├── apple_jobs_ranked.csv
│   ├── amazon_jobs_ranked.csv
│   ├── oracle_jobs_ranked.csv
│   └── ...
├── cover_letters/               # Generated cover letters
│   └── {Company}_{Role}_Cover_Letter.txt
└── outreach_emails/             # Networking emails
    └── CDF_Volunteer_Application.txt
```

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
- Read `references/personal_details.md` for personal info, education, experience, and skills
- Read `references/projects.md` for available projects

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
- Update `resumes/resume.html` with tailored content
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
| AI Automation Engineer | AgenticAI, N8N, CRE Agent (RAG), Lambda Microservices, Resumade |

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
| **AI Automation / Integration / Agentic AI / Workflow** | AI Automation Resume | `Harsha_Yellela_AI-Automation-Engineer.pdf` |
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
- `Harsha_Yellela_AI-Automation-Engineer.pdf` - AI Automation / Agentic AI focused

---

## Job Application Tracking

**IMPORTANT:** After successfully submitting ANY job application (Indeed, LinkedIn, or any other platform), Claude MUST update the job applications CSV file.

### CSV File Location
`D:\Desktop\resume\job_tracking\job_applications.csv`

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

## CRITICAL: Role Matching Before Applying

**STOP and verify role fit BEFORE applying to any job. Do NOT bulk-apply without vetting.**

### Harsha's Core Competencies (APPLY TO THESE)
| Category | Skills/Experience |
|----------|-------------------|
| **ML/AI** | LLM fine-tuning (QLoRA), deep learning, NLP, computer vision, MLOps pipelines |
| **Backend** | Python (FastAPI), Go, Node.js, REST APIs, microservices |
| **DevOps** | Kubernetes, AWS (Lambda, EKS, SageMaker), Docker, CI/CD, Terraform |
| **Data** | PostgreSQL, MongoDB, Redis, data pipelines |

### DO NOT APPLY (Immediate Skip)
| Role Type | Reason |
|-----------|--------|
| **Splunk/SIEM/Security Analytics** | No Splunk experience |
| **Salesforce/SAP/Oracle ERP** | No enterprise ERP experience |
| **iOS/Swift Development** | No iOS experience |
| **Mainframe/COBOL** | Not relevant to background |
| **Federal Security Clearance Required** | F-1 OPT visa status |
| **10+ years experience required** | Only 2-3 years experience |
| **Staff/Principal/Director level** | Too senior |
| **Domain-specific tools** (Workday, ServiceNow admin, etc.) | No experience |

### Role Matching Checklist (Before Each Application)
1. **Read the job title carefully** - Does it match ML/AI, SDE, Backend, DevOps, or Full Stack?
2. **Check required skills** - Can Harsha demonstrate 60%+ of required skills?
3. **Check experience level** - Is it entry-level, mid-level (2-5 years), or senior (5+ years)?
4. **Check for deal-breakers** - Security clearance? Specific tools not in skillset?
5. **If uncertain, ASK** - Better to skip than waste time on a bad fit

### When Bulk Applying
- **Flag mismatches** to user before submitting
- **Group by fit level**: TOP PICK (>80% match), HIGH (60-80%), STRETCH (40-60%), SKIP (<40%)
- **Prioritize quality over quantity** - 10 good matches > 50 random applications

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
| AI Automation, Integration, Agentic AI, Workflow | `Harsha_Yellela_AI-Automation-Engineer.pdf` |
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
1. **Create folder** (if not exists): `cover_letters/`
2. **File naming**: `{Company}_{Role}_Cover_Letter.txt`
   - Example: `EY_MLE_Cover_Letter.txt`
3. **Tailor content** to match:
   - Job requirements from posting
   - Harsha's relevant experience from `references/JOB_APPLICATION_CONTEXT.md`
   - Specific technologies mentioned in JD
4. **Format**: Plain text, professional business letter format
5. **Inform user** of file location so they can upload manually if needed

### Cover Letter Template Structure:
```
V Harsha Vardhan Yellela
36631 Jefferson Ct, Apt 814, Farmington Hills, MI 48335
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
- Cover letters in `cover_letters/` are temporary
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

## Networking Contacts & Referrals

**Active Referral Contacts:**

| Contact | Company | Connection | Status | Notes |
|---------|---------|------------|--------|-------|
| **Professor Tina Korani** | Apple (via husband) | Met at LTU Research Day (Apr 2025) | Pending outreach | Associate Professor at SJSU, offered to help with Apple referral |
| **Maral Mesma Khosroshahi** | Microsoft | LinkedIn outreach | Pending (sent 2026-01-16) | Senior Researcher - AI/ML/LLMs, Foundation Models |
| **Arian Hosseini** | Microsoft | LinkedIn outreach | Pending (sent 2026-01-16) | Tech Lead PhD, UIUC - mutual connection Tina Korani |
| **Reza Soroushmehr** | Microsoft | LinkedIn outreach | Pending (sent 2026-01-16) | Senior SWE - Applied AI/ML, Azure LLM training |
| **Arman Khondker** | Microsoft | LinkedIn outreach | Pending (sent 2026-01-16) | SWE - CoreAI/Copilot, multimodal speech LLMs |

**Referral Tracking File:** `job_tracking/referral_requests.csv`

---

## Dream Job Reference

**AI Engineer (New Graduate) @ Distyl**

| Field | Details |
|-------|---------|
| Company | Distyl (AI-native systems for Fortune 1000) |
| Role | AI Engineer (New Graduate) |
| Location | On-site: San Francisco or New York |
| Salary | $150,000 - $170,000 |
| Type | Full-Time, Entry Level / New Grad |
| Backers | Lightspeed, Khosla, Coatue, OpenAI partners |
| Leadership | Veterans from Palantir, Apple, national research labs |

**Why This is Perfect:**
- Build production LLM systems from day one
- RAG pipelines, agent logic, evaluation, tooling
- LangChain/LlamaIndex frameworks (Harsha's expertise)
- AWS/cloud experience valued (bonus)
- Customer-facing work + technical depth
- Equity, 401(k), benefits, cutting-edge AI tools

**Apply Link:** https://lnkd.in/gHk_pwqs (Workstory.io)
**Recruiter:** John Loubser (Job Placement Specialist) - Messaged on LinkedIn 2026-01-17
**LinkedIn Post:** https://www.linkedin.com/feed/update/urn:li:activity:7418184919639805952/
**Source:** Brother sent this job listing
**Status:** Applied 2026-01-17 ✓ (Video intro + resume + cover letter submitted via Workstory.io)

---

**Contact Details:**
- **Tina Korani:** tina.korani@sjsu.edu | Discord: tkorani | LinkedIn: tinakorani
  - Background: UX/UI expert, Co-founder Immersive Storytelling Lab at SJSU
  - Connection: Husband works at Apple, offered referral for ML/SDE roles

**Additional User Accounts:**
- **Alternative Email:** harshavardhan.yellela@gmail.com (used for academic/networking correspondence)
- **Discord:** har5ha
- **Workstory.io:** harsha.yellela@gmail.com (Google OAuth login)
  - Video uploaded: "AI Engineer Introduction - Harsha Yellela"
  - Resume uploaded: ml_engineer
  - Equipment: Brio 100 microphone, NVIDIA Broadcast camera

---

## Build Fellowship (Accepted - January 2026)

| Field | Value |
|-------|-------|
| Program | Build Fellowship - Build Projects |
| Project | Build and train transformer language model |
| Role | Student Consultant |
| Build Fellow | Kacper Raczy |
| Schedule | Tuesdays 6:00 PM ET, 8 weeks (start TBD) |
| Commitment | 1-2 hrs/week + 60-min weekly workshop |
| Requirements | Attend 5/8 workshops, final deliverable, Pre/Post surveys |
| Contact | education@buildfellowship.com |

**Action Items:**
- [ ] Confirm participation via link (by EOD Sun Jan 25)
- [ ] Complete Pre-Project Survey when received (by EOD Sun Jan 25)
- [ ] Sign up for Orientation: Wed Jan 28, 5pm ET
- [ ] Watch for email from Kacper Raczy (Build Fellow) by end of week
- [ ] Reply to Kacper's email + RSVP calendar invite

**Project Details:** Develop a text generation language model using GPT/transformer architecture with attention mechanism. State-of-the-art NLP techniques.

---

## Current Volunteer Position (OPT Status Maintenance)

**INTERNAL - Do not mention externally**

| Field | Value |
|-------|-------|
| Organization | Community Dreams Foundation (CDF) |
| Role | Machine Learning Engineer (Volunteer) |
| Start Date | February 2, 2026 |
| Type | Nonprofit volunteer - maintains F-1 OPT status |
| Slack | ML/AI department channel |
| Working Hours | 9:00–18:00 EST |

**Purpose:** Volunteer work at qualifying nonprofits helps maintain OPT status while job hunting. Light workload - primarily for status maintenance.

**Channels:**
- #general - Project postings (don't post intros here)
- Department-specific channel - Post intro, look for project matches
- #payment_queries, #onboarding_queries, #waiver_queries, #other_queries - Support channels

---

## Task Log

**Instructions for Claude:** After completing any significant task, add an entry here with the date and description. Keep entries concise. **Only keep the last 4 entries** - delete older ones when adding new. This helps future chat sessions understand the project state.

### Log Entries

| Date | Task Completed | Details |
|------|----------------|---------|
| 2026-01-22 | Build Fellowship accepted + CDF prep | Accepted to Build Fellowship "transformer language model" project (Kacper Raczy). CDF volunteer starts 02/02/26 |
| 2026-01-23 | Created open-source template | Published job-application-llm-agent to GitHub with template files, skills, and comprehensive README. Repo: https://github.com/HAR5HA-7663/job-application-llm-agent |
| 2026-02-10 | Merge conflicts resolved | Pulled remote, resolved 3 conflicts (CLAUDE.md, job_applications.csv, personal_details.md), merged all entries |
| 2026-02-10 | AI Automation Engineer resume | Created `resumes/html/ai_automation_engineer.html` with MCP, Bedrock, function calling, structured output, RAG skills. Added to all tracking tables |

### Pending/In Progress
- **Build Fellowship (by EOD Sun Jan 25):** Confirm participation, Pre-Project Survey, Orientation signup (Jan 28)
- Send email to Professor Tina Korani for Apple referral
- Complete Akraya ML Engineer chatbot questions
- Microsoft referral requests sent (4 contacts pending response)
- Distyl application submitted - awaiting response from recruiter John Loubser
- Total applications: 304 (CSV job_applications.csv)
- CDF: Starts 02/02/26, look for ML/AI projects in department channel

---

## Agent Learnings & Tips for Future Sessions

**Browser Extension Issues:**
- If browser extension is not connected, user needs to:
  1. Make sure Chrome is open with the Claude extension installed
  2. May need to restart Chrome after installation
  3. Must be logged into claude.ai with the same account as Claude Code
- Report issues at: https://github.com/anthropics/claude-code/issues

**Job Application Efficiency:**
- Always check role fit BEFORE applying (see "CRITICAL: Role Matching" section)
- Use the skill `job-applicator` for streamlined applications
- Batch similar roles together for faster processing
- Keep job_applications.csv updated after EVERY successful submission

**File Reading Order on New Session:**
1. CLAUDE.md (this file) - for context and instructions
2. temp.txt - for any queued messages from previous session
3. job_applications.csv - to know current count and recent activity
4. personal_details.md / JOB_APPLICATION_CONTEXT.md - only when actively applying

**Common User Patterns:**
- Typos in commands are intentional - parse for intent, don't ask for clarification
- "i did it continue" = user completed a manual step, proceed
- User wants autonomous action, not confirmation dialogs
- Use tables for status summaries - user likes structured output

### Current State Summary
- **Folder Structure:** Organized into 6 folders (resumes, references, job_tracking, ranked_jobs, cover_letters, outreach_emails)
- **Projects:** 27 total in `references/projects.md`
- **Applications:** 260 tracked in `job_tracking/job_applications.csv`
- **Resumes:** 5 variants (SDE, ML, DevOps, AI-Automation, General) + HTML sources in `resumes/html/`

---

*End of CLAUDE.md*
