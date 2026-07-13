📚 Smart Semantic Search System using ChromaDB

A Python-based School Knowledge Assistant that uses ChromaDB to perform semantic search on school-related documents. Instead of relying on exact keyword matching, the system understands the meaning of a user's query and retrieves the most relevant information.

🚀 Features
Persistent ChromaDB database
Collection: school_documents
40+ school-related documents
Natural language semantic search
Retrieves the Top 3 most relevant documents
Displays:
Document ID
Retrieved Document
Similarity Distance
Command-line interface (CLI)
🛠️ Technologies Used
Python
ChromaDB
Vector Database
Semantic Search
Natural Language Processing (NLP)
📂 Project Structure
├── app.py
├── school_db/
└── README.md
▶️ How to Run
python app.py

Enter your question in natural language, for example:

What are the school timings?
How can I get admission?
Can students use mobile phones?
When is the Parent Teacher Meeting?
Does the school provide transport?

The system returns the three most relevant documents based on semantic similarity.

🎯 Learning Objectives
Build a persistent vector database with ChromaDB
Store and manage documents
Implement semantic search using embeddings
Retrieve relevant information using natural language queries
