
This project is a Retrieval-Augmented Generation (RAG) chatbot that uses an agentic architecture to answer user questions based on uploaded documents. It uses a message-passing protocol called **Model Context Protocol (MCP)** to coordinate communication between agents and ensure modularity and traceability.

---


- ✅ Supports document uploads in multiple formats:
  - PDF, DOCX, PPTX, CSV, TXT / Markdown
- ✅ Agent-based architecture with:
  - `IngestionAgent`: parses and preprocesses documents
  - `RetrievalAgent`: performs semantic retrieval using embeddings and FAISS
  - `LLMResponseAgent`: formulates final query and generates the answer
- ✅ Uses structured messages via **Model Context Protocol (MCP)**
- ✅ Hugging Face GPT-2 model (no API key needed)
- ✅ GitHub-renderable `.ipynb` (no widgets)
- ✅ Provides final answer + top source chunks for traceability

---


| Component            | Tool / Library                  |
|----------------------|----------------------------------|
| Embeddings           | `sentence-transformers` (MiniLM) |
| Vector DB            | `FAISS`                          |
| LLM                  | Hugging Face `gpt2`              |
| Document Parsing     | `PyMuPDF`, `python-docx`, `pptx`, `pandas` |
| UI                   | Google Colab (can be extended to Streamlit) |
| Messaging Protocol   | Custom `MCPMessage` class        |

---

User ➝ IngestionAgent ➝ RetrievalAgent ➝ LLMResponseAgent ➝ Answer
│ │ │
PDF/PPTX/CSV Embeddings Prompt + LLM
+ FAISS



├── Agentic_RAG_Chatbot_MCP.ipynb   ← Cleaned notebook (no widgets)
├── README.md                       ← This file
├── architecture.pptx               ← System architecture slides
├── sample_doc.pdf                  ← Example document to test chatbot
├── requirements.txt                ← Optional (dependencies)

