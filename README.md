# Multimodal RAG System for Car Image & Specification Retrieval

This project implements a **multimodal Retrieval-Augmented Generation (RAG) system** that retrieves car images and specifications using **CLIP image embeddings**, **MiniLM text embeddings**, and **FAISS vector search**. The system answers user queries by combining image similarity search, text-based retrieval, and LLM-powered response generation.

---

## 🚀 Key Features

- **Multimodal Embeddings**
  - CLIP for image features (car brands/models)
  - MiniLM for text embeddings (specifications)

- **Semantic Search with FAISS**
  - Fast and accurate nearest-neighbor search

- **RAG Pipeline with LlamaIndex**
  - Retrieves relevant text chunks from specification files

- **LLM-Powered Answer Generation**
  - Uses Gemini to generate contextual and factual responses
  - Combines retrieved images + specs for grounded outputs

- **Custom Car Dataset**
  - Scraped dataset of 4 car brands
  - Images + detailed specifications

- **Interactive Querying with Gradio UI**
  - Users type any query and receive:
    - Relevant car image
    - Retrieved car specifications
    - A Gemini-generated answer

---

## 🧠 System Architecture

### 1. **Embedding Layer**
- CLIP → image vector representations  
- MiniLM → text spec embeddings  

### 2. **Vector Store**
- FAISS index for image and text retrieval  
- Stores millions of vectors efficiently  

### 3. **RAG Layer**
- LlamaIndex retrieves top-k relevant text chunks  
- CLIP retrieves top-k similar car images  

### 4. **LLM Layer**
- Gemini combines:
  - Retrieved image metadata  
  - Relevant car specs  
  - User query  
- Produces one consolidated answer  

### 5. **User Interface**
- Gradio front-end for querying and displaying:
  - Output image  
  - Matched specs  
  - Final LLM response  

---

## 🛠️ Tech Stack

**Python, CLIP, MiniLM, FAISS, LlamaIndex, Gemini API, Gradio, Pandas, NumPy**

---

## 📂 Project Structure

dataset/
images/
specs.csv

src/
embeddings.py
vectorstore.py
rag_pipeline.py
llm_engine.py
app.py

ui/
gradio_interface.py

requirements.txt
README.md
