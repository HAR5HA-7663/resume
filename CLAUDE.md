# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

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
| 2024-12-25 | DevOps resume | Created DevOps-focused resume with 6 projects (Telegram K8s, ML Sentiment Loop, Online Learning Portal Jenkins, Lambda IaC, Car Dealer K8s, Job Portal Docker) |
| 2024-12-25 | Indeed job apps | Applied to 3 DevOps positions: Principal Engineer at Etactics ($90K-$105K), DevOps Engineer at Etactics ($75K+), Platform Engineer at Brooksource ($125K-$145K) |
| 2024-12-25 | Job context file | Created JOB_APPLICATION_CONTEXT.md - comprehensive context file for LLM/browser agents to fill job application forms automatically |
| 2024-12-27 | General portfolio resume | Created versatile portfolio resume showcasing 6 high-profile projects: QLoRA LLM fine-tuning, MLOps microservices, Lambda (94 functions), Go backend, ROS Robotics, Graph Neural Networks |

### Pending/In Progress
- Ready for new job descriptions or applications

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
