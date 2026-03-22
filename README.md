# ai-text-summarizer
#  AI Text Summarizer

A lightweight full-stack application that converts unstructured text into structured insights using an LLM-inspired workflow. The application processes messy input text and returns a concise summary, key points, and sentiment analysis in a clean and user-friendly interface.

---

##  Overview

This project demonstrates how unstructured text can be transformed into structured data using prompt-based logic. It follows a clean client-server architecture with a React frontend and a Node.js backend.

The system is designed to be simple, reliable, and easy to extend with real LLM APIs such as OpenAI or Google Gemini.

---

##  Features

* Accepts unstructured / messy text input
* Generates:

  * One-line summary
  * Three key points
  * Sentiment (positive / neutral / negative)
* Clean and responsive UI
* Backend validation and error handling
* Mock LLM implementation for stable demo
* Easily extendable to real AI APIs

---

##  Tech Stack

### Frontend

* React.js
* Vite
* Axios
* HTML5 & CSS3

### Backend

* Node.js
* Express.js
* CORS

### AI Layer

* Prompt-based structured output design
* Mock LLM function (replaceable with real API)

---

##  Project Structure

```
ai-text-summarizer/
│
├── frontend/
│   ├── src/
│   │   ├── App.js
│   │   ├── index.css
│   ├── package.json
│
├── backend/
│   ├── server.js
│   ├── package.json
│   ├── .env
│
└── README.md
```

---

## ⚙️ Setup Instructions

### 1️ Clone the repository

```
git clone <your-repo-link>
cd ai-text-summarizer
```

---

### 2 Setup Backend

```
cd backend
npm install
npm start
```

Backend runs on:

```
http://localhost:5001
```

---

### 3️ Setup Frontend

```
cd frontend
npm install
npm run dev
```

Frontend runs on:

```
http://localhost:3000 (or 3001 if busy)
```

---

##  API Endpoint

### POST `/api/summarize`

**Request:**

```json
{
  "text": "Your unstructured text here"
}
```

**Response:**

```json
{
  "summary": "The text describes a mixed user experience.",
  "keyPoints": [
    "Users find the app fast",
    "There are performance issues",
    "Users have mixed opinions"
  ],
  "sentiment": "neutral"
}
```

---

## Prompt Design

The system is designed around structured output generation using strict constraints:

* One-sentence summary
* Exactly 3 key points
* Controlled sentiment labels
* JSON-only output format

This ensures consistency and easy parsing.

---

##  LLM Integration Strategy

This project follows an LLM-first design but uses a **mock implementation** for stability.

### Why Mock LLM?

* Avoid API failures during demo
* Ensure predictable output
* Remove dependency on external services

### Production Upgrade

The mock function can be easily replaced with:

* OpenAI API
* Google Gemini API

---

##  Trade-offs & Decisions

* Used mock LLM instead of real API for reliability
* Kept a single API endpoint for simplicity
* Minimal UI to focus on functionality
* No authentication (not required for scope)

---

## 🔮 Future Improvements

* Integrate real LLM APIs (OpenAI / Gemini)
* Add file upload support (PDF, TXT)
* Improve summarization logic using NLP
* Add user authentication
* Deploy to cloud (Vercel / Render)

---

## 📸 Example Output

**Input:**

```
hiiii!!! this app sooo good??? fasttt but sometimes laggg...
users like it but also complain?? weird experience!!!
```

**Output:**

```
Summary:
The text describes a mixed user experience with both positive and negative aspects.

Key Points:
- Users find the app fast and good
- There are occasional performance issues
- Users have mixed opinions

Sentiment:
Neutral
```

---

##  Key Learnings

* Designing structured prompts for consistent output
* Building full-stack applications with clean architecture
* Handling real-world API limitations
* Implementing fallback strategies for reliability

---

##  Author

**Yeddula Ganesh Maruthi**

* B.Tech (AI & ML)
* Interested in Full Stack Development, AI/ML, and UI/UX

---

##  Final Note

This project focuses on clarity, reliability, and strong fundamentals rather than complexity. It demonstrates the ability to design, build, and explain an LLM-powered workflow in a production-ready manner.

---
