# 🚀 CareerPath.AI - Intelligent Career Coaching Agent

**CareerPath.AI** is a multi-agent system designed to act as a personalized career coach. It helps users navigate their professional journey by analyzing resumes, generating learning roadmaps, and conducting mock interviews.

Built using **Python** and **Google's Gemini 2.0 Flash**, this project demonstrates advanced agentic patterns including sequential processing, state management, and context engineering.

---

## 🧠 Key Features

* **Resume Analysis**: Detects requests for CV reviews and provides constructive feedback using LLM capabilities.
* **Personalized Learning Roadmaps**: Generates step-by-step study plans for specific technologies (e.g., "Learn Python for Data Science").
* **Mock Interview Prep**: Simulates interview questions based on the user's target role.
* **Context Awareness**: Remembers previous parts of the conversation to provide coherent, follow-up advice (e.g., remembering you are a beginner when suggesting a roadmap).
* **Multi-Agent Architecture**: Uses a coordinator to orchestrate specialized agents (Intent Classifier + Generative Reply).

---

## 🏗️ Architecture

The system follows a **Sequential Multi-Agent** architecture:

1.  **Coordinator**: The central hub that manages data flow.
2.  **Memory Module**: Stores conversation history (Session State).
3.  **Intent Agent (Rule-Based)**: Analyzes user input to determine the goal (Resume, Roadmap, Interview, or General).
4.  **Reply Agent (LLM-Powered)**: Uses **Gemini 2.0 Flash** with context injection to generate high-quality, human-like responses.

### Workflow
`User Input` -> `Coordinator` -> `Memory Log` -> `Intent Classification` -> `Context Retrieval` -> `LLM Generation` -> `Response`

---

## 🛠️ Tech Stack

* **Language**: Python 3.10+
* **LLM Provider**: Google Gemini API (`gemini-2.0-flash`)
* **Libraries**: `google-generativeai`, `dataclasses`, `json`
* **Environment**: Jupyter Notebook / Kaggle Kernel

---

## ✅ Capstone Requirements Met

This project satisfies the **Agents Intensive** course requirements by implementing:

1.  **Agent powered by an LLM**: Utilizes `gemini-2.0-flash` for dynamic reasoning and content generation.
2.  **Sequential Agents**: Implements a pipeline where the *Intent Agent's* output guides the *Reply Agent's* behavior.
3.  **Sessions & State Management**: A custom `Memory` class persists conversation history across turns.
4.  **Context Engineering**: Dynamically injects conversation history and detected intent into the LLM system prompt.

---

## 🚀 Getting Started

### Prerequisites
1.  A Google account.
2.  A free API Key from [Google AI Studio](https://aistudio.google.com/).
3.  Python installed on your machine.

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/mandarvisave/career-path-agent.git
    cd CareerPath-AI
    ```

2.  **Install Dependencies**
    ```bash
    pip install google-generativeai
    ```

3.  **Set up your API Key**
    Open the notebook (`careerpath-ai.ipynb`) and locate the configuration cell:
    ```python
    import os
    # Replace with your actual key
    os.environ["GOOGLE_API_KEY"] = "AIzaSyD-Your-Actual-Key-Here"
    ```

4.  **Run the Agent**
    Run all cells in the Jupyter Notebook. The final cell contains a testing loop to demonstrate the agent's capabilities.

---

## 🧪 Usage Example

**User**: "I need to learn Python for Data Science."
**Agent**: "Great choice! Here is a 3-step roadmap: 1. Master syntax & loops. 2. Learn Pandas & NumPy. 3. Build a regression project."

**User**: "Can you check my resume?"
**Agent**: "I can certainly help. Please paste your resume text here so I can review your formatting and keywords."

---

## 🔮 Future Improvements

* **Tool Integration**: Add Google Search capability to find real-time job postings.
* **RAG (Retrieval Augmented Generation)**: Upload PDF resumes for deeper analysis.
* **Frontend**: Build a Streamlit or Gradio UI for a better user experience.

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
