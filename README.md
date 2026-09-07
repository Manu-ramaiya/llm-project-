# llm-project-
What is included
ResumeAI_Project/
│
├── app.py                 # FastAPI backend + RAG + analysis + agent logic
├── requirements.txt       # Python dependencies
├── .env.example           # Optional LLM configuration
├── .gitignore
├── README.md              # Complete GitHub README
├── PROJECT_BRIEF.txt      # Short project description
│
├── uploads/
│
└── static/
    ├── index.html         # Website UI
    ├── style.css          # Responsive styling
    └── app.js             # Frontend functionality
🚀 Project Overview

ResumeAI — AI Resume Reviewer & Career Advisor

ResumeAI is a web-based AI career assistant that helps students tailor their resumes for specific job roles.

The user can:

Upload a resume PDF
Paste resume text
Enter a target job role
Upload job-description PDFs
Use RAG to retrieve relevant job requirements
Analyze resume-job alignment
Identify missing skills
Receive resume-review feedback
Get an interview preparation roadmap
Generate a personalized 3-month learning plan
Core Architecture
                    Resume PDF
                        │
                        ▼
                Resume Extraction
                        │
                        ▼
              ┌─────────────────┐
              │ Resume Analyzer │
              └────────┬────────┘
                       │
                       │
Job Description PDF ──► RAG Retrieval
                       │
                       ▼
               Relevant Job Context
                       │
                       ▼
              ┌─────────────────┐
              │ Resume Reviewer │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Career Advisor  │
              └────────┬────────┘
                       │
          ┌────────────┼─────────────┐
          ▼            ▼             ▼
       Score      Missing Skills   Interview
                                      │
                                      ▼
                              3-Month Learning
                                    Plan
🧠 RAG Implementation

The prototype implements:

PDF → Text → Chunking → TF-IDF → Cosine Similarity → Relevant Context

This keeps the project lightweight and lets you run it locally without needing a vector database or API key.

🤖 Agent Components

Resume Reviewer

Checks role alignment
Finds matching skills
Identifies skill gaps
Provides resume improvement suggestions

Career Advisor

Prioritizes missing skills
Creates interview preparation steps
Creates the 3-month learning roadmap
📊 Website Output

The dashboard displays:

Resume Score /100
Alignment verdict
Matched skills
Missing skills
Resume reviewer feedback
Career advisor recommendations
Interview preparation roadmap
RAG-retrieved job-description context
3-month personalized learning plan
