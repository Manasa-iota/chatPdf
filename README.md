# PDF Chat App

A web application where users can **upload PDFs** and **ask questions**, with answers generated **only from the content of the uploaded PDFs**.

## Features
- PDF Upload – Users can upload one or multiple PDFs.
- Question Answering – Ask questions in natural language and receive accurate, context-aware answers.
- Semantic Search – Retrieves only relevant chunks of text from PDFs for precise responses.
- Vector Database – FAISS is used for fast and efficient similarity search.

## How It Works
1. Extract & Chunk PDF Text – The uploaded PDFs are read and split into smaller text chunks for better search performance.
2. Generate Embeddings – PDF chunks are converted into vector embeddings using Google Generative AI embeddings.
3. Store in FAISS – The embeddings are stored in a FAISS vector database to enable quick semantic search.
4. Retrieve & Answer – LangChain retrieves the most relevant chunks and generates answers based solely on the uploaded PDFs.

## Tech Stack
- Frontend: Streamlit (for quick UI)
- Backend: Python
- PDF Processing: PyPDF2
- Text Splitting: LangChain’s RecursiveCharacterTextSplitter
- Embeddings: Google Generative AI Embeddings
- Vector Store: FAISS
- Retrieval & Answering: LangChain

## Installation
- git clone https://github.com/Manasa-iota/chatPdf.git
- cd chatPdf 
- pip install -r requirements.txt

## Usage
streamlit run app.py

1. Upload your PDF(s) via the UI.
2. Ask your question in the input box.
3. Get context-aware answers instantly.
