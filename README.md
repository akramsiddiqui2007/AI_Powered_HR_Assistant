# 🤖 AI-Powered HR Assistant  
*A Conversational Chatbot built using OpenAI GPT-3.5, LangChain, and Gradio*

---

## 📋 Project Overview

This project demonstrates how to build an **AI-powered HR Assistant** capable of answering employee queries from an **HR policy document**.  
The assistant extracts, embeds, and retrieves relevant information from the policy PDF, and generates context-aware answers using **OpenAI GPT-3.5-Turbo**.

The project showcases:
- Integration of **OpenAI’s GPT & Embeddings API**
- Use of **LangChain** for text chunking, retrieval, and prompt management  
- **ChromaDB** for vector storage and semantic search  
- A **Gradio Web UI** for interactive chatbot experience  
- Optional **conversation memory** and **chat logging**

---

## 🧩 Architecture

### 🧠 System Flow

```text
User Query
   ↓
Gradio Chat Interface
   ↓
LangChain Q&A Pipeline
   ↓
Retriever → Chroma Vector DB → OpenAI Embeddings
   ↓
GPT-3.5 Turbo → Generates Final Response
   ↓
Answer Displayed to User
```


## ⚙️ Setup Instructions
🧱 1. Clone this Repository
git clone https://github.com/yourusername/AI_Powered_HR_Assistant.git
cd AI_Powered_HR_Assistant


## 🔑 2. Add Your OpenAI API Key
In your terminal or notebook:
export OPENAI_API_KEY="your_openai_api_key"
or
import os
os.environ["OPENAI_API_KEY"] = "your_openai_api_key"


## 📦 3. Install Required Dependencies
pip install -r requirements.txt

If you encounter SQLite issues with Chroma:
pip install pysqlite3-binary


## 🚀 Running the Project
🧮 Step-by-Step Notebook Flow
| Step       | Description                                       |
| ---------- | ------------------------------------------------- |
| **Step 1** | Environment Setup & Imports                       |
| **Step 2** | Load and Split HR Policy PDF                      |
| **Step 3** | Generate Embeddings & Build Vector Store (Chroma) |
| **Step 4** | Build Q&A Chain with OpenAI GPT-3.5               |
| **Step 5** | Launch Gradio Chatbot Interface                   |
| **Step 6** | Add Conversation Memory, Logging & Evaluation     |


## ▶️ To Launch Chatbot UI
Run the last cell in your notebook or:
jupyter notebook Crafting_an_AI_Powered_HR_Assistant.ipynb
Then open the Gradio link (usually http://127.0.0.1:7860 or a gradio.live public URL).

# 🧠 Features
Natural Language Querying — Ask questions directly from the HR policy.
Context-Aware Responses — GPT-3.5 uses retrieved document chunks for accurate answers.
Interactive UI — Powered by Gradio.
Memory & Logging — Maintains conversation continuity and logs all Q&A pairs.
Modular Code — Each step (1–6) can be reused for any corporate policy chatbot.


## 🗂 Example Questions
| User Question                                   | Example Answer                                                                                                                |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| What is the policy on employee training?        | The HR policy emphasizes continuous learning and development through on-the-job training, leadership programs, and mentoring. |
| How does the company ensure work-life balance?  | Flexible working conditions and supportive management are key aspects of the work-life balance strategy.                      |
| What is the approach toward employee relations? | The company fosters mutual trust, respect, and dialogue with employees, ensuring fair and constructive relationships.         |


## 📄 File Structure
```text
AI_Powered_HR_Assistant/
│
├── Crafting_an_AI_Powered_HR_Assistant.ipynb   # Main Notebook
├── the_nestle_hr_policy_pdf_2012.pdf            # HR Policy Document
├── requirements.txt                             # Dependencies
├── chat_log.csv                                 # Interaction logs (auto-created)
├── architecture_diagram.png                     # Architecture Diagram
└── README.md                                   # Project Overview (this file)
```

## 📊 Results & Evaluation
| Metric            | Description                          |
| ----------------- | ------------------------------------ |
| Response Accuracy | 85–95% depending on query complexity |
| Avg Response Time | ~2.5 seconds per question            |
| Model Used        | OpenAI GPT-3.5-Turbo (2024-05 API)   |
| Embedding Model   | text-embedding-3-small               |


## 🤝 Acknowledgements
#### OpenAI API for GPT-3.5 and Embeddings
#### LangChain Framework for building modular pipelines
#### ChromaDB for vector-based retrieval
#### Gradio for UI deployment
#### HR policy reference from Nestlé Human Resources Policy (2012)

