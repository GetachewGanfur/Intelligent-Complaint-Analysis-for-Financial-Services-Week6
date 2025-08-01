# Intelligent-Complaint-Analysis-for-Financial-Services-Week6

This project builds a Retrieval-Augmented Generation (RAG) system using consumer complaint data from the CFPB. It allows users to ask questions and get AI-generated answers based on real complaint narratives.

---

## 🔧 Project Tasks

### 1. EDA & Preprocessing

- Loaded CFPB dataset and explored product types and complaint lengths.
- Filtered for 5 products:
  - Credit card
  - Personal loan
  - Buy Now, Pay Later
  - Savings account
  - Money transfers
- Removed empty narratives and cleaned text (lowercase, remove boilerplate, special chars).
- 📁 Output: `filtered_complaints.csv` in `data/`

### 2. Text Chunking & Embedding

- Long texts split into chunks (`chunk_size=500`, `overlap=50`).
- Used `all-MiniLM-L6-v2` embedding model.
- Stored embeddings in FAISS index with metadata.
- 📁 Output: Vector store in `vector_store/`

### 3. RAG Logic & Evaluation

- Implemented a retriever to get top-5 relevant chunks per question.
- Designed a prompt template for generation.
- Used an LLM to generate answers based on retrieved context.
- Evaluated with a sample of 10 questions.
- 📁 Output: Code in `src/rag_pipeline.py`, evaluation in `evaluation/rag_eval_report.md`

### 4. Interactive Interface

- Built using **Streamlit**.
- Features:
  - Input box for questions
  - Answer display with source chunks
  - Clear/reset button
- 📁 Output: `src/ui_app.py`

---

## 🛠️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/GetachewGanfur/Intelligent-Complaint-Analysis-for-Financial-Services-Week6.git
   cd Intelligent-Complaint-Analysis-for-Financial-Services-Week6
   ```
