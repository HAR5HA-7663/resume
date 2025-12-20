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
| Backend/SDE | Resumade.in, AgenticAI |
| ML/AI Engineer | Sentiment Forecasting, Pneumonia Detection |
| Data Scientist | Sentiment Forecasting |
| Full Stack | Resumade.in, Pneumonia Detection |
| Cloud Engineer | All (emphasize AWS components) |
| Healthcare AI | Pneumonia Detection |

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

## Task Log

**Instructions for Claude:** After completing any significant task, add an entry here with the date and description. Keep entries concise. This helps future chat sessions understand the project state.

### Log Entries

| Date | Task Completed | Details |
|------|----------------|---------|
| 2024-12-20 | Initial setup | Created `personal_details.md` and `projects.md` context files |
| 2024-12-20 | Extracted existing data | Populated both files with data from `resume.html` (4 projects, personal info, skills) |
| 2024-12-20 | Updated CLAUDE.md | Added instructions for adding projects, tailoring resumes from JD, and session continuity |

### Pending/In Progress
- Awaiting user to provide additional projects to add to `projects.md`

### Current State Summary
- **Projects in projects.md:** 4 (Resumade.in, Sentiment Forecasting, AgenticAI, Pneumonia Detection)
- **personal_details.md:** Complete with education, experience, skills, achievements
- **resume.html:** Contains current resume (can be tailored per JD)

---

*End of CLAUDE.md*
