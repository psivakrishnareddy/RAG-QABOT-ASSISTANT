# RAG-QABOT-ASSISTANT
# QA Bot with LangChain and LLM

A question-answering bot that leverages LangChain and Large Language Models to answer questions from PDF documents.

## Overview

This application enables users to upload PDF documents and ask questions about their content. The bot uses retrieval-augmented generation (RAG) to provide accurate answers based on the document content.

## Features

- PDF document upload and processing
- Natural language question answering
- Interactive web interface using Gradio
- Vector-based document retrieval
- Chunk-based document processing

## Prerequisites

- Python 3.11
- Virtual environment setup

## Installation

1. Create and activate virtual environment:
```bash
pip install virtualenv
virtualenv my_env
source my_env/bin/activate
```

2. Install required packages:
```bash
python3.11 -m pip install \
    gradio==4.44.0 \
    ibm-watsonx-ai==1.1.2 \
    langchain==0.2.11 \
    langchain-community==0.2.10 \
    langchain-ibm==0.1.11 \
    chromadb==0.4.24 \
    pypdf==4.3.1 \
    pydantic==2.9.1
```

## Usage

1. Run the application:
```bash
python3.11 qabot.py
```

2. Access the web interface at port 7860
3. Upload a PDF document
4. Type your question in the query box
5. Submit to receive an answer

## Technical Details

- Uses Mixtral 8x7B as the base LLM
- Implements document chunking with RecursiveCharacterTextSplitter
- Uses ChromaDB for vector storage
- Employs IBM's Slate 125M English embeddings model
- Implements RAG using LangChain's RetrievalQA

<img width="1297" alt="RAG BOT" src="https://github.com/user-attachments/assets/bdb0afe4-9129-49ce-88b3-9dd51104e24c" />



## Note

For optimal performance, use moderately sized PDF documents. Large documents may not process successfully with the current configuration.
