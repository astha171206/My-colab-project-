📚 AI Research Paper & Intelligent System

📌 Project Overview


The AI Research Paper & Intelligent System is an AI-powered application designed to simplify research paper discovery and analysis using Natural Language Processing (NLP), Large Language Models (LLMs), and semantic search.


The system preprocesses research paper datasets, extracts meaningful entities using a Hybrid Named Entity Recognition (NER) architecture, converts text into vector embeddings, and retrieves the most relevant research papers using FAISS and Cosine Similarity. It also integrates ChatGroq through LangChain to provide intelligent, context-aware responses to user queries.


🚀 Features


📂 Research paper dataset loading and preprocessing

🧹 Text cleaning and tokenization

🤖 Sentence embedding generation

🧠 Hybrid Named Entity Recognition (NER)

⚡ Fast semantic search using FAISS

📊 Cosine Similarity-based document retrieval

💬 ChatGroq-powered intelligent responses

🔗 LangChain integration for LLM orchestration

🔍 Context-aware research paper search

📑 Data filtering using Pandas (iloc)

📄 Research paper summarization


🧰 Technologies & Tools Used


Programming Language

Python

AI & LLM


ChatGroq

Groq API

LangChain


NLP & Machine Learning


Sentence Transformers

Hugging Face Transformers

Hybrid Named Entity Recognition (NER)

Cosine Similarity

Scikit-learn

Vector Search


FAISS (Facebook AI Similarity Search)

Data Processing


Pandas

NumPy

Development Environment

Google Colab

🔄 Project Workflow


Load the research paper dataset.

Clean and preprocess the text.

Generate sentence embeddings using Sentence Transformers.

Extract entities using Hybrid NER.

Store vector embeddings in FAISS.

Accept the user's research query.

Convert the query into vector embeddings.

Retrieve the most relevant research papers using Cosine Similarity and FAISS.

Pass the retrieved context to ChatGroq through LangChain.

Generate an intelligent response based on the retrieved papers.

