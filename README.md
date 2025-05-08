# 📘 Personalized Study Assistant with AutoGen

An intelligent, multi-agent system that automates the creation of personalized study plans, quizzes, and content summaries based on user-provided syllabi or topics. Built using **[AutoGen](https://github.com/microsoft/autogen)**.

---

## 🧠 Features

- 📅 **Study Plan Generator**  
  Automatically breaks a syllabus into a weekly study schedule.

- 📝 **Quiz Creator**  
  Generates multiple-choice, short-answer, and conceptual questions from text.

- 📚 **Summarizer Agent**  
  Summarizes long readings or YouTube lecture transcripts.

- 💬 **Q&A Tutor**  
  Allows the student to ask questions and receive helpful, contextual answers using **RAG (Retrieval-Augmented Generation)**.

- 🔄 **Feedback Loop**  
  Learner can rate content quality, and agents iterate to improve over time.

---

## 🧩 Architecture Overview

The system uses multiple AutoGen agents that collaborate in a pipeline:

### 📌 Planner Agent
- Takes input syllabus (text, PDF, or topic list)
- Breaks down content into weekly units

### 📌 Content Agent
- For each unit, retrieves or generates relevant study content (summaries, readings, or video links)

### 📌 Quiz Agent
- Generates quizzes based on each unit's content
- Uses LLMs with rule-based logic to ensure variety and relevance

### 📌 Tutor Agent
- Interactive chatbot for student questions
- Pulls from study material and optional external sources

### 📌 Evaluator Agent *(Optional)*
- Collects user feedback on quiz quality and summary clarity
- Flags content for revision or improvement

---

## 🛠️ Tech Stack

- 🧠 **AutoGen (Microsoft)**
- 🐍 **Python** (LangChain / LLM utilities)
- 💬 **OpenAI API** or **LLaMA 3** for local deployment
- 🖥️ **Streamlit** or **Gradio** for user interface
- 📄 **PyMuPDF** or **pdfplumber** for syllabus parsing
- 🎥 **YouTube Transcript API** for lecture video summarization

---

## 🚀 How It Works

```bash
1. User uploads syllabus or list of topics
2. Planner Agent outputs a week-by-week breakdown
3. Content Agent fills each week with readings, summaries, and lectures
4. Quiz Agent generates custom quizzes
5. Tutor Agent supports interactive questions throughout the learning process

