<div align="center">
 
  <h1>ApplyWise AI </h1>
  <p><strong>Your Intelligent Career Copilot</strong></p>

  [![Website](https://img.shields.io/badge/Live_Website-applywisehq.com-blue?style=for-the-badge&logo=vercel)](https://applywisehq.com)
  [![Chrome Extension](https://img.shields.io/badge/Chrome_Extension-Available-orange?style=for-the-badge&logo=googlechrome)](https://chromewebstore.google.com/detail/applywise-ai/malcjkgaacojabhipjbbdhamknpfhefi)
  [![Made with Next.js](https://img.shields.io/badge/Built_with-Next.js_14-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
  [![Powered by Gemini](https://img.shields.io/badge/Powered_by-Google_Gemini-4285F4?style=for-the-badge&logo=google)](https://deepmind.google/technologies/gemini/)

  *Note: To protect proprietary algorithms and business logic, the core codebase for ApplyWise is currently closed-source. This repository serves as a public tracker for feature requests, bug reports, and an architectural overview of the platform.*
</div>

---

## 🎯 What is ApplyWise?

**ApplyWise** is a full-stack SaaS platform and Chrome Extension designed to eliminate the friction from modern job hunting. By leveraging advanced LLMs (Google Gemini), ApplyWise automates ATS compliance checking, personalizes cover letters instantly, and tracks job applications across the web via a drag-and-drop Kanban board.

## ✨ Core Features Engineered

### 1. AI-Powered ATS Resume Scanner
A high-performance file parsing engine that extracts text from PDFs and DOCX files to run advanced keyword matching algorithms via Gemini AI. Built to handle heavy loads with robust IP-based rate limiting and error handling.

### 2. Context-Aware Chrome Extension
A bundled React-based Chrome Extension that dynamically injects AI functionality into major job boards (LinkedIn, Indeed). It scrapes the active job description DOM in real-time and securely communicates with the Next.js backend to generate completely tailored Cover Letters on the spot.

### 3. Application Tracking (Kanban Dashboard)
A fluid, drag-and-drop interface built for the user dashboard. Job applications are persisted via Prisma/PostgreSQL, fully synced with the Chrome Extension, and managed through React state and Framer Motion animations.

### 4. Dynamic Generation & Storage Pipelines
Users maintain multiple resumes and default profiles, which are seamlessly merged with incoming job descriptions. Generating personalized CV tweaks and tracking the resulting artifacts required complex asynchronous state management and secure NextAuth implementation.

---

## 🏗️ Technical Architecture

ApplyWise is built on a modern, scalable serverless stack:

- **Frontend:** React 18, Next.js 14 (App Router), Tailwind CSS, Framer Motion
- **Backend:** Next.js Server Actions & API Routes, Node.js
- **Database:** PostgreSQL managed via Prisma ORM
- **Authentication:** NextAuth.js (OAuth integrations)
- **AI Integration:** Google Gemini Pro API (with custom prompt engineering and fallback logic)
- **File Processing:** `pdf-parse` and `mammoth` for robust document extraction
- **Infrastructure:** Vercel (Edge caching, serverless deployments)

### System Flow
1. **Client Interaction:** Whether via the web portal or the Chrome Extension, input data (Resumes/JDs) is captured and validated.
2. **Secure Verification:** Endpoints enforce strict Auth and Rate Limiting (`checkRateLimit()`) before allowing resource-intensive AI operations.
3. **LLM Pipeline:** Data is fed into fine-tuned Gemini API endpoints using structured prompt templates to ensure consistent, highly formatted JSON responses.
4. **Data Persistence:** User actions, generated artifacts, and tracking metrics are managed relationally in PostgreSQL.

---


## 🛣️ Roadmap & Issue Tracking

While the code is private, we build in public.

- **Found a Bug?** Please open an issue in this repository using the `bug` tag.
- **Feature Request?** Submit an issue using the `enhancement` tag. We actively monitor this repo for user feedback!

---

## 👨‍💻 About the Creator

Built and maintained by **Haris Khan**.

- **GitHub:** [@haris0207](https://github.com/haris0207)
- **LinkedIn:** [haris0207](https://www.linkedin.com/in/haris0207/)
- **Contact:** [Email](hariskhan0207@gmail.com)

If you are a recruiter, investor, or developer interested in the technical details or system design behind ApplyWise, I am more than happy to jump on a call and do a live code walk-through!

<div align="center">
  <sub>Built with ❤️ and too much coffee.</sub>
</div>
