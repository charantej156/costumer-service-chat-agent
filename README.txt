Project Name: AI-Powered E-Commerce Customer Service Chat Agent

Problem Statement:
E-commerce platforms struggle with handling a large volume of customer inquiries efficiently. Traditional customer support solutions often lead to long response times, high operational costs, and inconsistent information delivery. There is a need for an AI-powered solution that can provide accurate and instant responses to customer queries by leveraging existing documentation and knowledge bases.

Solution:
This project introduces an AI-driven customer service chat agent that utilizes document-based retrieval and NLP models to deliver accurate responses. By processing and indexing product details, FAQs, and policies, the chat agent ensures seamless customer interactions. The system employs FAISS for efficient document retrieval and advanced LLMs for high-quality response generation, significantly improving response times and customer satisfaction.

Description:
This project is an AI-driven customer service chat agent designed for e-commerce platforms. It leverages document-based retrieval and NLP models to provide accurate and efficient responses to customer inquiries. The chat agent processes PDFs, DOCX, and TXT files containing product details, FAQs, and policies to generate meaningful responses. It is built using Python (Flask) for the backend and Streamlit for the user interface, ensuring a seamless customer support experience.

Features:
Document-based customer service chat agent.

AI-driven response generation using NLP models.

Uses FAISS for efficient document retrieval.

Streamlit-based UI for a user-friendly experience.

Supports PDF, DOCX, and TXT file processing.

Utilizes Large Language Models (LLMs) for response generation.

Technologies Used:

Programming Language: Python

Web Framework: Flask, Streamlit

NLP Models:SentenceTransformers (all-MiniLM-L6-v2) for text embedding and semantic search.

Hugging Face Transformers (Flan-T5) for text-to-text generation and response formulation.

Document Handling: PyPDF2, docx2txt

Vector Search: FAISS (Facebook AI Similarity Search)

How It Works:

Uploaded documents are processed and chunked into smaller text segments.

Each text segment is converted into vector embeddings using SentenceTransformers.

FAISS indexes these embeddings for efficient retrieval.

When a user submits a query, the system converts it into an embedding and searches FAISS for the most relevant document chunks.

The retrieved text chunks are combined and passed to the Flan-T5 model, which generates a coherent and contextually appropriate response.

Installation Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/charantej156/costumer-service-chat-agent.git
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # For macOS/Linux
   venv\Scripts\activate  # For Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the chat agent application:
   ```bash
   streamlit run app.py
   ```

5. Open the chat agent in a browser:
   The chat agent UI will open automatically via Streamlit.

File Structure:
```
Ecommerce-Chatbot/
│── app.py  # Main Flask/Streamlit application
│── data/
│   ├── docs/  # Directory for storing customer service documents
│── models/
│   ├── nlp_model.py  # AI Model integration
│── requirements.txt  # Python dependencies
│── README.txt  # Project Documentation
```

Usage:
- Upload e-commerce-related documents (FAQs, policies, product details).
- Ask the chat agent questions related to the uploaded documents.
- The chat agent retrieves the most relevant response using FAISS and NLP models.

