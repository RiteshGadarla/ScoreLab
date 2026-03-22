# Score Lab
**AI-Powered Teacher Assistant for Automated Grading and Personalized Feedback** 🌟  
*Submission for the Google Solutions Challenge 2025 by Telugu Techies*

**Demo Video**: [Video](https://drive.google.com/drive/folders/1juSpKeuLp69iLn3VBU-Z59GXkJ3lx9lI?usp=sharing) 🎥


## Overview 📖
Teachers worldwide are overburdened with manual grading and struggle to provide personalized feedback, especially in large or under-resourced classrooms. This limits their ability to mentor effectively and deprives students of tailored guidance essential for learning.

**Score Lab** is an AI-powered platform that automates student answer script evaluation using the **Gemini API** 🤖. Teachers upload question papers and students submit answers as PDFs, which are analyzed by AI to deliver accurate scores and detailed feedback instantly. By streamlining the evaluation process, Score Lab saves time ⏱️, reduces teacher workload, and enhances student learning outcomes, aligning with **UN SDG 4: Quality Education** 🌍.

---

## Team Details 👥
- **Team Name**: Telugu Techies
- **Team Leader**: Ritesh Reddy G
- **Problem Statement**: Overburdened Teachers and the Need for Personalized Feedback

---

## Problem Statement ⚠️
- **Teacher Burden**: Manual grading is time-intensive and scales poorly with class size.
- **Feedback Gaps**: Students lack consistent, personalized feedback in large or resource-constrained settings.
- **Educational Equity**: Overworked teachers can’t ensure quality support for all learners.

---

## Our Solution 💡
**Score Lab** leverages AI to transform the evaluation process:
- **Teachers**: Upload question papers via a user-friendly dashboard 📤.
- **Students**: Submit answer scripts as PDFs and view scores/feedback on a performance dashboard 📊.
- **AI**: The Gemini API evaluates descriptive answers, while Document AI scans PDFs, providing instant, consistent results stored in Cloud SQL 🗃️.

This reduces manual effort, ensures unbiased scoring, and delivers actionable feedback to students—empowering teachers and enhancing education quality.

---

## Unique Selling Proposition (USP) ✨
Unlike existing tools that rely on structured inputs or manual grading, Score Lab:
- Automatically evaluates **handwritten descriptive answers** from PDFs using the Gemini API 📝.
- Delivers **instant marks and personalized feedback** without requiring rigid formats ⚡.
- Reduces teacher workload while improving student learning—uncommon in current solutions 🌟.

---

## Key Features 🛠️
- **Automatic Evaluation**: Gemini API assesses descriptive answers from PDFs 🤖.
- **Instant Feedback**: Generates scores and detailed feedback for each submission ⚡.
- **Student Dashboard**: Tracks marks and progress over time 📈.
- **Consistent Scoring**: Ensures unbiased, standardized evaluation ✅.
- **Teacher Relief**: Reduces grading burden with automation ⏳.
- **Student-Friendly**: Provides clear, actionable feedback to support learning 📚.

---

## Tech Stack 💻
- **Frontend**: Next.js (TypeScript), Tailwind CSS 🎨
- **Backend**: Next.js API Routes (`app/api/*`), Cloud Functions ⚙️
- **Database**: Cloud SQL (`lib/db.ts`) 🗄️
- **Storage**: Google Cloud Bucket (`lib/googleStorage.ts`) ☁️
- **AI/ML**: Gemini API (evaluation), Document AI (PDF scanning, `app/api/general/ocr.ts`) 🧠
- **Hosting**: Cloud Run 🚀
- **Development**: Project IDX, Google APIs 🛠️
- **Visualization**: Recharts (`StudentTasksChart.tsx`) 📊

---

## Project Structure 📂
```
google/
├── app/                    # Next.js app directory
│   ├── api/               # API routes (e.g., uploadAssignment, getpdf) ⚙️
│   ├── dashboard/         # Admin, teacher, student dashboards 📊
│   ├── user/              # Login/signup pages 🔐
│   ├── globals.css        # Global styles 🎨
│   └── layout.tsx         # Root layout 🏗️
├── components/            # UI components (e.g., sidebar.tsx, chart.tsx) 🧩
├── lib/                   # Utilities (db.ts, googleStorage.ts) 🛠️
├── public/                # Static assets (e.g., geminiLogo.png) 🖼️
├── .env.example           # Environment variables 🔑
├── next.config.mjs        # Next.js config ⚙️
├── package.json           # Dependencies 📦
└── tsconfig.json          # TypeScript config 📝
```

---

## Installation ⚙️
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Ritesh2006M/google.git
   cd google
   ```
2. **Install Dependencies**:
   ```bash
   npm install
   ```
3. **Set Up Environment**:
    - Rename `.env.example` to `.env.local` and add credentials (e.g., Gemini API key, Cloud SQL details) 🔑.
4. **Run the Application**:
   ```bash
   npm run dev
   ```

---

## Process Flow 🔄
1. **Teacher**: Uploads question paper PDF (`teacher/upload/page.tsx`) 📤.
2. **Student**: Submits answer script PDF (`student/uploadAssignment/route.ts`) 📝.
3. **AI Processing**:
    - Document AI scans PDFs (`app/api/general/ocr.ts`) 📑.
    - Gemini API evaluates answers and generates scores/feedback 🤖.
4. **Storage**: Results saved to Cloud SQL and files to Cloud Bucket 🗃️.
5. **Dashboard**: Students view performance (`dashboard/student/page.tsx`) 📊.

---

## Architecture Diagram 🏛️
```
[Teacher] ----> [Question Paper PDF] ----> [Cloud Bucket] ☁️
[Student] ----> [Answer Script PDF] ----> [Cloud Bucket] ☁️
                       |
                  [Document AI] 📑
                       |
                 [Gemini API] 🤖 ----> [Cloud Functions] ⚙️
                       |
                 [Cloud SQL] 🗄️ <----> [Next.js App] 💻
                       |
[Dashboards: Admin, Teacher, Student] 📊
```

---

## Future Development 🚀
- **Multi-Format Support**: Expand beyond PDFs to images, handwritten notes 📸.
- **Exportable Reports**: Generate performance summaries for teachers 📋.
- **Multi-Language**: Support evaluation in additional languages 🌐.
- **Admin Role**: Enhanced management features (`dashboard/admin/*`) 👩‍💼.
- **Gamification**: Add student incentives (e.g., badges) 🎮.
- **Plagiarism Detection**: Integrate checks for originality 🔍.
- **Scheduling**: Automate assignment deadlines ⏰.
- 
---

## Team 👥
- **Ritesh Reddy G** (Team Leader)
- **Rohan Rao G**
- **Sai Shobit K**
- **Jayansh Aditya**
---

*Built by Telugu Techies to empower educators and students for the Google Solutions Challenge 2025.* 🌟

