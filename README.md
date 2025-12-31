🤖 AI Assistant Helper

AI-powered Email Assistant & README Generator

Turn your GitHub repositories into professional READMEs ✨
and streamline your inbox using AI-driven insights.

🔗 Repository: https://github.com/Sagar-Admane/Ai-assistant-helper

📌 Overview

AI Assistant Helper is a full-stack AI-powered email assistant designed to simplify inbox management.
It securely connects to your Gmail account, fetches recent emails, and uses an AI model to:

Generate concise summaries

Categorize emails (Work, Personal, Finance, etc.)

Suggest actionable next steps like Reply, Add to Calendar, or Ignore

The application features a clean, interactive dashboard built with React and a robust backend powered by Node.js, Express, and TypeScript.

✨ Features
🔐 Authentication

Dual authentication support:

Email & Password

Google OAuth 2.0

📩 Email Fetching

Retrieves the 10 most recent Gmail emails using the Gmail API

Read-only access for enhanced security

🧠 AI-Powered Analysis

For any selected email, the AI:

Generates a short, readable summary

Classifies the email (Work, Personal, Finance, etc.)

Suggests an action:

Reply (auto-generates subject & body)

Add to Calendar (extracts event details)

Ignore

🖥️ Interactive Dashboard

Clean UI to browse emails

One-click AI analysis

Modal-based action confirmation

🔗 Webhook Integration

Sends structured AI output to a webhook endpoint

Enables automation with external tools and workflows

🛠️ Technology Stack
Frontend

React

TypeScript

Vite

SASS

Axios

React Router

Material-UI (Modals)

Backend

Node.js

Express

TypeScript

MongoDB (Mongoose)

JWT Authentication

Google APIs (Gmail API, OAuth 2.0)

OpenRouter API (AI model access)

📁 Project Structure
.
├── backend/        # Node.js / Express backend
│   ├── src/        # TypeScript source code
│   ├── dist/       # Compiled JavaScript output
│   ├── .env        # Environment variables (must be created)
│   └── package.json
│
└── frontend/       # React client
    ├── src/        # React + TypeScript source
    │   └── Components/
    └── package.json

⚙️ Setup & Installation
Prerequisites

Node.js v18+

npm or yarn

MongoDB (local or cloud)

🔧 Backend Setup
cd backend
npm install


Create a .env file inside backend/:

PORT=4000
MONGO=mongodb://localhost:27017/your_db_name
SECRET=your_jwt_secret
SALT=10

# Google OAuth
CLIENT_ID=your_google_client_id
CLIENT_SECRET=your_google_client_secret
REDIRECT_URI=http://localhost:4000/oauth2callback

# AI API
OPENAI_KEY=your_openrouter_api_key


Run the backend server:

npm run dev


Backend will run on:
👉 http://localhost:4000

🎨 Frontend Setup
cd frontend
npm install
npm run dev


Frontend will be available at:
👉 http://localhost:5173

🔄 How It Works

Authentication

User logs in via email/password or Google OAuth

Gmail Integration

App fetches the 10 most recent emails (read-only access)

Dashboard View

Displays sender & subject of recent emails

AI Analysis

Clicking an email sends content to /ai/ai-helper

AI returns structured JSON:

Summary

Category

Suggested action

User Confirmation

AI suggestions shown in a modal

User confirms action

Automation

Confirmed data is sent to a webhook endpoint

Simulates integration with external services

🔌 API Endpoints
Method	Endpoint	Description
GET	/login	Initiates Google OAuth
GET	/oauth2callback	OAuth callback
GET	/emails	Fetch recent Gmail emails
POST	/ai/ai-helper	AI email analysis
GET	/userinfo	Fetch logged-in user info
🚀 Example Use Cases

AI-assisted inbox triaging

Automated email summarization

Workflow automation via webhooks

Productivity tools for professionals

❤️ Made With Love

Made with ❤️ by @Sagar-Admane
