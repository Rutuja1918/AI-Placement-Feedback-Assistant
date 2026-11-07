# 🎯 AI Placement Feedback Assistant

An AI-powered interview preparation application built using **Python, LangGraph, Streamlit, and LLMs**. It helps students practice technical interviews, evaluate their answers, identify improvement areas, and receive personalized feedback.

## 🚀 Project Overview

The AI Placement Feedback Assistant simulates a technical interview experience. Users can select their target career role, generate or enter interview questions, submit answers, and receive AI-powered evaluation and feedback.

## ✨ Features

- **Career Role Selection:** Choose a target job role for interview practice.
- **AI Question Generation:** Generate technical interview questions.
- **Manual Question Input:** Enter custom interview questions.
- **Answer Analysis:** Analyze student responses.
- **Answer Evaluation:** Evaluate answers and assign scores.
- **Personalized Feedback:** Generate suggestions for improvement.
- **Final Report:** Create an interview performance report.
- **Conditional Workflow:** Use LangGraph conditional routing based on evaluation scores.
- **Tracing and Monitoring:** Monitor workflow execution using LangSmith.

## 🛠️ Technologies Used

- Python
- LangGraph
- LangChain
- Streamlit
- Google Gemini / configured LLM provider
- LangSmith
- Python-dotenv

## 🧠 Workflow Architecture

The application uses a stateful LangGraph workflow.

```text
START
  |
  v
Analyze Answer
  |
  v
Evaluate Answer
  |
  v
Conditional Routing
  |
  |-- Score < 7 --> Feedback
  |                    |
  |                    v
  |                 Report
  |
  |-- Score >= 7 --> Report
                         |
                         v
                        END
```

## 📂 Project Structure

```text
AI-Placement-Feedback-Assistant/
│
├── app.py
├── state.py
├── nodes.py
├── graph.py
├── requirements.txt
├── README.md
├── .gitignore
└── .env
```

**Note:** The `.env` file is excluded from GitHub and must be created locally.

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Rutuja1918/AI-Placement-Feedback-Assistant.git
cd AI-Placement-Feedback-Assistant
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

Windows:

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure environment variables

Create a `.env` file in the project directory and add the API credentials required by your configured LLM provider and LangSmith.

Never upload API keys or secrets to GitHub.

### 6. Run the application

```bash
streamlit run app.py
```

The application will open in your browser at `http://localhost:8501`.

## 📌 Learning Outcomes

- Understanding LangGraph State and workflow architecture.
- Creating and connecting workflow nodes and edges.
- Implementing conditional routing.
- Integrating LLMs into an application.
- Building an interactive application using Streamlit.
- Monitoring AI workflow execution using LangSmith.

## 👩‍💻 Author

**Rutuja Holmukhe**

BE Information Technology Student

GitHub: [Rutuja1918](https://github.com/Rutuja1918)

---

⭐ If you find this project useful, feel free to explore the repository!