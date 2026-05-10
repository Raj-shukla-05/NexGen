# NexGen - AI-Powered Interview Preparation & Resume Architect

NexGen is an advanced, AI-driven platform designed to empower job seekers by providing personalized interview preparation and tailored resume generation. By leveraging the power of Generative AI, NexGen bridges the gap between a candidate's current profile and their dream job.

## 🚀 What This Project Does

NexGen takes three primary inputs from the user: their **Resume (PDF)**, a **Self-Description**, and the **Target Job Description**. It then provides:

1.  **AI Interview Report**:
    *   **Match Score**: A percentage-based evaluation of how well the candidate fits the role.
    *   **Technical & Behavioral Questions**: A curated list of potential interview questions, the interviewer's intention behind them, and structured guidance on how to answer.
    *   **Skill Gap Analysis**: Identifies missing skills and categorizes them by severity (Low, Medium, High).
    *   **Personalized Preparation Plan**: A day-wise roadmap (Day 1, Day 2, etc.) with specific tasks to bridge gaps and prepare for the role.
2.  **Tailored Resume Generation**:
    *   Generates a professional, ATS-friendly resume tailored specifically to the provided job description.
    *   Converts AI-generated HTML into a high-quality downloadable PDF.
3.  **Secure Authentication**: User accounts with JWT-based authentication to save and manage multiple interview reports.

## 🛠 Tech Stack

### Frontend
*   **Framework**: [React](https://react.dev/) (via Vite)
*   **Styling**: [Sass (SCSS)](https://sass-lang.com/)
*   **Routing**: React Router v7
*   **Icons**: Lucide React
*   **HTTP Client**: Axios

### Backend
*   **Runtime**: [Node.js](https://nodejs.org/)
*   **Web Framework**: [Express.js](https://expressjs.com/)
*   **Database**: [MongoDB](https://www.mongodb.com/) (using Mongoose ODM)
*   **Authentication**: JSON Web Tokens (JWT) & BcryptJS
*   **File Handling**: Multer & PDF-Parse
*   **Automation**: [Puppeteer](https://pptr.dev/) (for HTML to PDF conversion)

### AI Integration
*   **Model**: [Google Gemini 3 Flash](https://deepmind.google/technologies/gemini/)
*   **SDK**: `@google/genai`
*   **Validation**: [Zod](https://zod.dev/) & `zod-to-json-schema` for strictly structured AI responses.

## 💡 The Problem Being Solved

The modern job market is highly competitive, and job seekers face several challenges:
1.  **Generic Resumes**: Most candidates use the same resume for every application, leading to low ATS scores and fewer callbacks.
2.  **Interview Anxiety**: Not knowing what questions to expect or how to structure answers leads to poor performance.
3.  **Vague Preparation**: Candidates often waste time studying irrelevant topics instead of focusing on the specific skills required for a role.
4.  **Skill Discovery**: It is difficult for candidates to objectively identify where they fall short compared to a job description.

**NexGen solves this** by providing a data-driven, objective, and actionable preparation strategy, ensuring candidates are not just applying, but are actually *ready*.

---

## 🏗 Getting Started

### Prerequisites
*   Node.js installed
*   MongoDB instance (local or Atlas)
*   Google Gemini API Key

### Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/Raj-shukla-05/NexGen.git
    cd NexGen
    ```

2.  **Setup Backend**:
    ```bash
    cd Backend
    npm install
    # Create a .env file and add:
    # PORT=3000
    # MONGO_URI=your_mongodb_uri
    # JWT_SECRET=your_secret
    # GOOGLE_GENAI_API_KEY=your_gemini_api_key
    npm start
    ```

3.  **Setup Frontend**:
    ```bash
    cd ../Frontend
    npm install
    npm run dev
    ```
