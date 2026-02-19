
# ⚖️ LexAI — Judicial Intelligence System

**LexAI** is a Retrieval-Augmented Generation (RAG) powered legal intelligence assistant designed to answer queries **strictly based on statutory data** from the **Indian Motor Vehicles Act**.

The system combines local Large Language Models with vector-based retrieval to deliver **grounded, citation-safe legal responses** without hallucinations.

---

## 🚀 Features

- 🔎 **RAG-based Architecture** (Retrieval + LLM grounding)
- 📚 Vector database powered by **ChromaDB**
- 🧠 Local LLM inference via **Ollama (Gemma)**
- 📄 Excel-based statutory ingestion pipeline
- ⚖️ Strict document-bound answering (no assumptions, no hallucinations)
- 🔒 Fully local and private execution
- 🎨 Premium **Streamlit** UI with judicial-themed design

---

## 🏗️ Architecture Overview
User Query
↓
Chroma Vector Store (Embeddings: mxbai-embed-large)
↓
Top-K Relevant Legal Sections
↓
Strict Grounded Prompt Template
↓
Gemma LLM (via Ollama)
↓
Final Answer (Statute-Only, No External Knowledge)


---

## 🛠️ Tech Stack

| Component        | Technology |
|------------------|------------|
| Frontend         | Streamlit |
| LLM Runtime      | Ollama |
| LLM Model        | gemma3:latest |
| Embeddings       | mxbai-embed-large |
| Vector Store     | ChromaDB |
| Framework        | LangChain |
| Data Source      | Structured Excel (Motor Vehicles Act provisions) |

---

## 📂 Project Structure
LexAI/
│
├── main.py # Streamlit application
├── vector.py # Vector ingestion & retrieval logic
├── converted_data.xlsx # Statutory legal dataset
├── chroma_docs_db2/ # Persisted Chroma embeddings
├── README.md
└── requirements.txt


---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/lexai.git
cd lexai
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Install Ollama & Required Models
Download Ollama from:
👉 https://ollama.com

Pull the required models:

ollama pull gemma3
ollama pull mxbai-embed-large
▶️ Running the Application
streamlit run main.py
The app will launch locally in your browser.

📊 Accuracy Evaluation
LexAI was evaluated using structured statutory queries covering:

Legal definitions

Penal provisions

Amendment references

Rule-making powers

Insurance and liability clauses

Observed Results
✅ High grounding reliability

✅ Accurate statutory quotations

✅ Correct fallback behavior when data is unavailable

Refer to LexAI_Accuracy_Report.txt for detailed evaluation metrics.

🧠 Hallucination Prevention Strategy
LexAI enforces a strict grounding protocol:

Answers must use only retrieved statutory records

External knowledge is explicitly disallowed

Mandatory fallback response:

"The data does not contain this information."

Additional safeguards include:

Context length control

Max Marginal Relevance (MMR) retrieval

Legal-domain optimized embeddings

🔐 Privacy & Security
🔒 100% local inference

🚫 No API calls

🌐 No external data transmission

💻 Fully offline capable

📈 Future Enhancements
Multi-Act support (IPC, CPC, CrPC)

Section-wise legal citation formatting

PDF ingestion pipeline

Legal citation confidence scoring

Hybrid search (BM25 + Vector embeddings)

Confidence estimation in responses

⚠️ Disclaimer
LexAI is an AI-powered legal research assistant.
It does not constitute legal advice.

For legal matters, always consult a qualified legal professional.

👨‍💻 Author
Developed as a Retrieval-Augmented Generation system for benchmarking statutory law accuracy using local LLMs.


---

If you want, I can also:
- Optimize this for **GitHub stars & recruiters**
- Add **badges** (Python, Streamlit, Ollama, License)
- Write a **strong project description** for resumes / LinkedIn
- Create a **system design diagram image**

Just say the word 😄

You said:
Everything as a copy paste version

ChatGPT said:
Perfect — here’s the clean, plain Markdown README you can directly copy-paste into README.md without changing anything.

⚖️ LexAI — Judicial Intelligence System
LexAI is a Retrieval-Augmented Generation (RAG) powered legal intelligence assistant designed to answer queries strictly based on statutory data from the Indian Motor Vehicles Act.

The system combines local Large Language Models with vector-based retrieval to deliver grounded, citation-safe legal responses without hallucinations.

🚀 Features
🔎 RAG-based Architecture (Retrieval + LLM grounding)

📚 Vector database powered by ChromaDB

🧠 Local LLM inference via Ollama (Gemma)

📄 Excel-based statutory ingestion pipeline

⚖️ Strict document-bound answering (no assumptions, no hallucinations)

🔒 Fully local and private execution

🎨 Premium Streamlit UI with judicial-themed design

🏗️ Architecture Overview
User Query
↓
Chroma Vector Store (Embeddings: mxbai-embed-large)
↓
Top-K Relevant Legal Sections
↓
Strict Grounded Prompt Template
↓
Gemma LLM (via Ollama)
↓
Final Answer (Statute-Only, No External Knowledge)

🛠️ Tech Stack
Component	Technology
Frontend	Streamlit
LLM Runtime	Ollama
LLM Model	gemma3:latest
Embeddings	mxbai-embed-large
Vector Store	ChromaDB
Framework	LangChain
Data Source	Structured Excel (Motor Vehicles Act provisions)
📂 Project Structure
LexAI/
├── main.py # Streamlit application
├── vector.py # Vector ingestion & retrieval logic
├── converted_data.xlsx # Statutory legal dataset
├── chroma_docs_db2/ # Persisted Chroma embeddings
├── README.md
└── requirements.txt

⚙️ Installation
1️⃣ Clone the Repository
git clone https://github.com/yourusername/lexai.git
cd lexai

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Install Ollama & Required Models
Download Ollama from:
https://ollama.com

Pull the required models:

ollama pull gemma3
ollama pull mxbai-embed-large

▶️ Running the Application
streamlit run main.py

The application will launch locally in your browser.

📊 Accuracy Evaluation
LexAI was evaluated using structured statutory queries covering:

Legal definitions

Penal provisions

Amendment references

Rule-making powers

Insurance and liability clauses

Observed Results
High grounding reliability

Accurate statutory quotations

Correct fallback behavior when data is unavailable

Refer to LexAI_Accuracy_Report.txt for detailed evaluation metrics.

🧠 Hallucination Prevention Strategy
LexAI enforces a strict grounding protocol:

Answers must use only retrieved statutory records

External knowledge is explicitly disallowed

Mandatory fallback response:

"The data does not contain this information."

Additional safeguards include:

Context length control

Max Marginal Relevance (MMR) retrieval

Legal-domain optimized embeddings

🔐 Privacy & Security
100% local inference

No API calls

No external data transmission

Fully offline capable

📈 Future Enhancements
Multi-Act support (IPC, CPC, CrPC)

Section-wise legal citation formatting

PDF ingestion pipeline

Legal citation confidence scoring

Hybrid search (BM25 + Vector embeddings)

Confidence estimation in responses

⚠️ Disclaimer
LexAI is an AI-powered legal research assistant.
It does not constitute legal advice.

For legal matters, consult a qualified legal professional.

👨‍💻 Author
Developed as a Retrieval-Augmented Generation system for benchmarking statutory law accuracy using local LLMs.
