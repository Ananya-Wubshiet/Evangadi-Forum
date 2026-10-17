# AI-Powered Evangadi Forum

A full-stack discussion platform that modernizes the community learning experience. This application extends a traditional forum with cutting-edge artificial intelligence, featuring semantic search, an AI writing assistant, and a private, document-based knowledge base powered by Retrieval-Augmented Generation (RAG).

### 🌐 [Click Here to View the Live Application](https://ananya-evangadi-forum.netlify.app/) 🚀
---

## 📌 Project Overview

Traditional forum architectures rely heavily on exact keyword matching, making information discovery rigid. The **AI-Powered Evangadi Forum** bridges this gap by utilizing AI vectors to understand user intent, context, and phrasing meaning. 

The application architecture is divided into three core functional pillars:

```text
                    AI-POWERED EVANGADI FORUM
                              |
          +-------------------+-------------------+

          |                   |                   |
          v                   v                   v
   Authentication       Forum & AI           Knowledge Base
   & Foundation         Assistance                / RAG

          |                   |                   |
          v                   v                   v
       Users          Questions & Answers     PDF & TXT Docs
       JWT            Semantic Search         Chunking
       Protected      Related Questions      Embeddings
       Routes         Draft Coach             Retrieval
                      Answer Fit              Grounded AI & Summary
```

---

## 🛠️ Technology Stack

| Architecture Layer | Technologies & Libraries Used |
| :--- | :--- |
| **Frontend Core** | React 19, Vite, React Router 7, Axios |
| **UI, Styling & UX** | CSS Modules, Framer Motion, Lucide React, React Markdown |
| **Backend Core** | Node.js, Express 5 (REST API Layer) |
| **Database & Storage** | MySQL 8+ (via `mysql2`), Local Static Storage |
| **Security & Auth** | JSON Web Tokens (JWT), bcrypt, Google Auth OAuth2 |
| **AI ecosystem** | Google Gemini AI (Text Models & Vector Embeddings) |
| **Communications** | Nodemailer (Gmail SMTP configuration) |

---

## 🚀 Core Features

### 🔐 1. Authentication & Security Framework
*   **Hybrid Authentication:** Supports traditional registration alongside official, branded Google OAuth Sign-In.
*   **Stateless Protection:** Secure token verification with JWT-based cookies/headers across protected API endpoints and React router guards.
*   **Identity & Validation:** Email ownership validation during account linking, bcrypt password hashing, and token-verified password reset workflows.
*   **Granular Profile Management:** User dashboards supporting dynamic avatar uploads (with live preview) and customizable profiles.
*   **Access Control:** Clear boundaries between **Admin** and **Member** tiers, enforced alongside resource ownership validations.

### 💬 2. Forums & Community Engagement
*   **Thread Lifecycles:** Create, read, update, and delete questions and answers with integrated Markdown text toolbar configurations.
*   **Granular Conversations:** Supports threaded sub-replies directly on answers for focused, itemized debates.
*   **Anti-Spam Restrictions:** Automated functional restrictions that prevent users from interacting with or validating their own posts.

### 🔍 3. Intelligent Search & Discovery Engine
*   **Hybrid Search Toggles:** Seamless real-time switching between standard MySQL keyword matching and AI vector-powered semantic search.
*   **Semantic Matching:** Computes vector embeddings on the fly, ranking relevance using **Cosine Similarity algorithms** across distinct phrased questions.
*   **Real-time Suggestions:** Highly optimized debounced search suggestion dropdown menus built smoothly into the global navbar.

### 🤖 4. Gemini AI Integrations
*   **AI Draft Coach:** Reviews and refines question formatting and clarity before a user submits them publicly.
*   **AI Answer Fit:** Evaluates answer accuracy and relevance relative to the root question thread.
*   **Fault-Tolerant Pipelines:** Native integration with OpenAI/Gemini systems featuring custom timeout, retry logic, and rate-limiting handles.

### 📚 5. Knowledge Base & RAG (Retrieval-Augmented Generation)
*   **Document Pipelines:** Upload, parse, and split PDF and TXT documents into optimized, searchable text chunks.
*   **Contextual Grounding:** Generates and queries vector embeddings on document chunks to serve contextually grounded AI responses.
*   **Summarization Presets:** One-click summarization utilizing specific style filters (Executive, Bullets, One-page) with native `.txt` and `.md` downloading capabilities.

---

## 📐 System Architecture

The project enforces an elegant, layered separation of concerns to maximize modular scalability and performance:

```text
                         React + Vite
                              |
                              | Axios (Bearer JWT)
                              v
                       Express REST API
                              |
          +-------------------+-------------------+

          |                   |                   |
          v                   v                   v
       Routes            Controllers          Middleware
                              |
                              v
                          Services
                       /     |      \
                      /      |       \
                     v       v        v
                  Forum      AI       RAG

                    |        |         |
                    v        v         v
                  Models   Gemini   Retrieval

                    |        |         |
                    v        v         v
                  MySQL   Embeddings  Documents
```

*   **Frontend Scope:** Manages application routing states, user authentications, application views, custom hooks, and dynamic layouts.
*   **Backend Scope:** Handles database connections, authorization policies, Gemini vector computations, semantic file streamings, and RAG chunking logic.

---

## 📦 Local Installation Guide

### Prerequisites
*   Node.js (v18 or higher)
*   MySQL Server (v8+)

### 1. Clone & Set Up Directory
```bash
git clone https://github.com
cd your-repo-name
```

### 2. Configure Environment Variables
Create a `.env` configuration file inside both the `/backend` and `/frontend` directories using your verified system parameters:

**Backend (`/backend/.env`):**
```env
PORT=5000
DB_HOST=localhost
DB_PORT=1234
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=evangadi_forum
JWT_SECRET=your_super_secure_jwt_secret
GEMINI_API_KEY=your_google_gemini_api_key
```

### 3. Run Applications Locally
Open two terminal windows to boot up both servers simultaneously:

```bash
# Terminal 1: Run Backend
cd backend
npm install
npm start

# Terminal 2: Run Frontend
cd frontend
npm install
npm run dev
```

---

## 📝 Milestone Summary
*   **Milestone 1:** Authentication & App Foundations — **Completed ✅**
*   **Milestone 2:** Questions, Answers & AI Assistants — **Completed ✅**
*   **Milestone 3:** Knowledge Base & RAG Pipeline Integration — **Completed ✅**

---
Developed with 💻 by Ananya Wubshiet.
