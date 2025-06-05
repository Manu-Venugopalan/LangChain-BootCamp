# 🔤 Text Embedding with OpenAI and Vectorization

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg) ![OpenAI](https://img.shields.io/badge/OpenAI-Embedding-blue.svg) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

This project demonstrates the generation of **text embeddings** using the **OpenAI API** and the transformation of those embeddings into numerical vectors suitable for downstream machine learning tasks such as clustering or classification.

---

## 🎯 Objective

The main goal of this notebook is to show how to:
- Generate dense vector representations for text (embeddings)
- Use OpenAI's `text-embedding-ada-002` model
- Store and analyze embeddings for text understanding and grouping
- Apply dimensionality reduction (e.g. PCA or t-SNE) and clustering techniques on the embedding space

---

## ⚙️ Features

- 🔹 Reads a dataset of text samples (CSV or JSON)
- 🔹 Generates OpenAI embeddings for each row
- 🔹 Stores embeddings with text in a structured dataframe
- 🔹 Optional: Performs clustering or dimensionality reduction
- 🔹 Visualizes high-dimensional data in 2D using t-SNE or PCA

---

## 🔄 Workflow

1. **Data Preparation**: Load text data from file into a pandas DataFrame
2. **Embedding Generation**:
   - Connect to OpenAI using API Key
   - Use `openai.Embedding.create()` with model `text-embedding-ada-002`
3. **Vector Storage**: Store embeddings in a NumPy array or DataFrame
4. **Optional Analysis**:
   - Apply PCA or t-SNE for visualization
   - Use clustering (e.g. KMeans) for document grouping

---

## 📁 Project Files

```
📦 Text-Embedding/
├── Text_embedding.ipynb               # Jupyter notebook with embedding logic
├── README_text_embedding.md           # Documentation
└── requirements_text_embedding.txt    # Required libraries
```

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/Text-Embedding.git
cd Text-Embedding
pip install -r requirements_text_embedding.txt
```

---

## 🧾 Requirements

```txt

```

Make sure to set your OpenAI API key using the environment variable:

```bash
export OPENAI_API_KEY="your-key-here"
```

---

## 💡 Use Cases

- Semantic search and document retrieval
- Text similarity and clustering
- Preprocessing for LLM-based classification
- Knowledge base vectorization for RAG systems

---

## 📄 License

This project is licensed under the MIT License.
