# RAG Q&A App

This is a Streamlit-based Retrieval-Augmented Generation (RAG) application that allows users to ask questions about content extracted from various types of documents including PDFs, DOCX, TXT files, raw text, and web URLs. It utilizes HuggingFace embeddings with FAISS indexing to retrieve relevant chunks and leverages the Meta-Llama-3-8B-Instruct model via HuggingFace's Inference API to generate answers.

## Features

- 📄 Supports document ingestion from:
  - PDF files
  - DOCX files
  - TXT files
  - Raw text
  - Web URLs
- 📚 Embeds document content using `sentence-transformers/all-mpnet-base-v2`
- 🔍 Uses FAISS for vector similarity search
- 🧠 Answers queries with the `meta-llama/Meta-Llama-3-8B-Instruct` LLM
- ⚡ Built with LangChain, HuggingFace, and Streamlit

## Installation

### 1. Clone the repository and create a virtual environment

```bash
git clone https://github.com/your-username/rag-qa-app.git
cd rag-qa-app
```

#### 1.1 Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate
```

### 2. Install dependencies

Ensure you have Python 3.8+ installed.

```bash
pip install -r requirements.txt
```

### 3. Configure API Key

```bash
export HUGGINGFACEHUB_API_TOKEN=your_huggingface_api_key
```

## Usage

### Run the App

```bash
streamlit run app.py
```

### How to Use

1. Select the input type from the dropdown:
   - Link
   - PDF
   - Text
   - DOCX
   - TXT
2. Upload or input the document accordingly.
3. Click **"Proceed"** to process the input and create a retriever.
4. Enter your query and click **"Submit"** to receive a generated answer.

## Project Structure

```
.
├── app.py                  # Main application logic
├── requirements.txt        # Required Python packages
└── README.md               # Project documentation
```

## Dependencies

Key Python libraries used in this project:

- `streamlit`
- `faiss-cpu`
- `langchain`
- `huggingface_hub`
- `sentence-transformers`
- `PyPDF2`
- `python-docx`

All dependencies are listed in `requirements.txt`.
