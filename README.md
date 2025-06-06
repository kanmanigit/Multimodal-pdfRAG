
# 🛍️ Multimodal RAG with LangChain, Milvus, and Unstructured

This project demonstrates a complete **Multimodal Retrieval-Augmented Generation (RAG)** pipeline that ingests unstructured PDF documents, extracts rich content (text, tables, and images), indexes them in Milvus, and answers user questions with reranked responses using LangChain and OpenAI.



## Environment Variables

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt





## 🚀 Features

- ✅ Extracts **text, tables, and images** from unstructured PDFs using `unstructured`
- 📂 Stores document embeddings in **Milvus** vector database
- 🤖 Uses **LangChain** to build RAG pipelines
- 🔁 Integrates **LLM-based reranking** using `LLMListwiseRerank`
- 📄 Supports metadata like content type and page numbers
- 🖼️ (Optional) Add custom **image embeddings** using CLIP/BLIP

## 🛠️ Tech Stack

| Layer            | Technology                                  |
|------------------|----------------------------------------------|
| Language         | Python 3                                     |
| Data Extraction  | [Unstructured](https://github.com/Unstructured-IO/unstructured) |
| Vector DB        | [Milvus](https://milvus.io)                  |
| Embeddings       | [Huggingface Embeddings]
| RAG Framework    | [LangChain](https://www.langchain.com)       |
| Reranker         | LLMListwiseRerank (via OpenAI GPT-4o)        |
| PDF Tools        | Tesseract, Poppler (for OCR and tables)      |
| (Optional) Image Embeddings | CLIP / BLIP via HuggingFace Transformers |



## 📦 Setup Instructions

### 1. Clone this repo

```bash
git clone git@github.com:kanmanigit/Multimodal-pdfRAG.git
cd multimodal-rag

### 2. Set up the environment

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

### 3. Add your API key
Create a .env file in the root directory with your OpenAI API key and Huggingface API key:
OPENAI_API_KEY=your_openai_api_key_here
HF_TOKEN=your_HF_TOKEN_api_key_here

### 2. Install dependencies
pip install -r requirements.

If you need OCR and image support:
brew install tesseract poppler  # macOS only


## Notes
Make sure your OpenAI key has access to GPT-4o.

## Project Structure
.
├── main.py                 # Main pipeline logic
├── sample.pdf              # Example PDF for demo
├── requirements.txt        # All dependencies
└── README.md               # This file

