# 🧾 Multi-format Document Loader using LangChain

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg) ![LangChain](https://img.shields.io/badge/LangChain-Framework-yellow.svg) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

This project demonstrates a utility for **loading documents in various formats (PDF, DOCX, TXT, JSON, etc.)** using the **LangChain** framework. It standardizes how documents from different sources are ingested for downstream tasks like retrieval, summarization, or LLM-powered processing.

---

## 🧠 Objective

The primary goal is to create a **modular document loader** that supports:

- `.pdf` via PyMuPDF, PyPDF2, and pdfplumber
- `.docx` via `python-docx`
- `.txt`, `.json`, and custom formats
- Directory-based and recursive file loading
- Seamless integration with LangChain pipelines

This tool is essential for preparing a document corpus for AI tasks such as Retrieval-Augmented Generation (RAG), chat-based assistants, or semantic search engines.

---

## ⚙️ Features

- ✅ Dynamically chooses the appropriate loader based on file extension
- ✅ Compatible with LangChain's `Document` abstraction
- ✅ Supports recursive folder scanning
- ✅ Easy to extend for other formats
- ✅ Clean and modular code with reusable functions

---

## 🔄 Workflow Summary

1. **File Scanning**: Uses `glob` and `os.walk` to collect paths for supported document types.
2. **Loader Dispatching**:
   - `.pdf`: Loaded using pdfplumber, PyMuPDF, or PyPDF2
   - `.docx`: Loaded via `Docx2TextLoader`
   - `.json`: Custom loader parses JSON text fields
   - `.txt`: Loaded using standard text file read
3. **LangChain Integration**:
   - Each file is converted to a LangChain `Document` object
   - Metadata such as file name or page number is attached
4. **Final Output**:
   - List of LangChain `Document` objects for downstream NLP or QA pipelines

---

## 📁 Project Structure

```bash
📦 Document-Loader/
├── document_loaders.ipynb        # Jupyter notebook with full implementation
├── README.md                     # Project documentation
└── requirements.txt              # Dependencies list
````

---

## 📦 Installation

To use this project:

```bash
git clone https://github.com/yourusername/Document-Loader.git
cd Document-Loader
pip install -r requirements.txt
```

---

## 🧾 Requirements

```txt
langchain
```

Optional additional packages you might need depending on how `.pdf` or `.docx` files are processed:

```txt
PyMuPDF
PyPDF2
pdfplumber
python-docx
```

---

## 🔍 Use Cases

* Preprocessing documents for RAG (Retrieval-Augmented Generation)
* Loading financial/legal documents for LLM chat assistants
* Converting diverse document formats into LangChain-compatible form

---
