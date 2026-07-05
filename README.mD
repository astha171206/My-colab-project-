AI Research Paper & Intelligent System
 Project Overview

This project is an AI-based Research Paper Intelligent System that helps in analyzing, searching, and retrieving relevant research papers using Natural Language Processing (NLP) and vector similarity techniques.

It converts text data into embeddings and finds similarity between sentences/papers using Cosine Similarity and FAISS indexing for fast retrieval.

 Key Features

Dataset loading and preprocessing
 Sentence transformation (cleaning, tokenization)
 Text Embedding generation
 Similarity calculation using Cosine Similarity
 Fast nearest neighbor search using FAISS
 Data filtering using .iloc
 Entity extraction and structured information handling
 Intelligent search for research papers


Technologies Used

Python 
Pandas (iloc for data handling)
NumPy
Scikit-learn
Sentence Transformers / NLP models
FAISS (Fast Approximate Nearest Neighbor Search) FAISS
Cosine Similarity

Dataset Description

The dataset includes research paper information such as:
Title
Abstract
Authors
Keywords
Entities / Named information
Paper ID
Data is cleaned and processed before embedding generation.

 Workflow of Project

1. Data Loading
import pandas as pd
df = pd.read_csv("dataset.csv")
df.head()
2. Data Selection using iloc
df = df.iloc[:, [0, 1, 2]]  # selecting required columns
3. Sentence Transformation (Text Preprocessing)
Lowercasing
Removing stopwords
Removing special characters
import re

def clean_text(text):
    text = re.sub(r'[^a-zA-Z]', ' ', text)
    return text.lower()

4. Embedding Generation
from sentence_transformers import SentenceTransformer

model = SentenceTransformer('all-MiniLM-L6-v2')
embeddings = model.encode(df['abstract'].tolist())

5. Cosine Similarity
from sklearn.metrics.pairwise import cosine_similarity
similarity = cosine_similarity(embeddings)

6. FAISS Indexing (Fast Search)
import faiss
import numpy as np

dimension = embeddings.shape[1]
index = faiss.IndexFlatL2(dimension)

index.add(np.array(embeddings))

7. Query Search Example
query = "machine learning in healthcare"
query_vec = model.encode([query])

distances, indices = index.search(np.array(query_vec), k=5)

Entity Recognition Module

The system also extracts entities like:
Research topic
Authors
Keywords
Organizations

This helps in better classification and intelligent search.

 Future Improvements

Web-based UI (Streamlit / Flask)
Better NLP model integration
Real-time research paper scraping
Advanced ranking system

 Author

Project: AI Research Paper Intelligent System
Language: Python
Domain: Artificial Intelligence & NLP Artificial Intelligence
