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
📌 GitHub Repository Description (Short)

Is short description ko GitHub repository ke Description field mein use karo:

A Python-based School Knowledge Assistant using ChromaDB for semantic search, enabling natural language queries to retrieve the most relevant school documents.

problem statement sab btao

Bilkul! Agar tum GitHub par upload kar rahi ho ya assignment submit karna hai, to ye complete documentation use kar sakti ho.

📚 Smart Semantic Search System using ChromaDB
📌 Project Title

Build a Smart Semantic Search System using ChromaDB

📖 Objective

The objective of this project is to build a semantic search system using ChromaDB that stores school-related documents in a persistent vector database. The system understands the meaning of a user's query and retrieves the most relevant documents instead of relying only on exact keyword matching.

❓ Problem Statement

Many schools store information in different documents such as admission policies, examination schedules, school rules, library information, transport details, fee policies, and announcements. Students often ask questions using different words than those used in the documents, making traditional keyword search less effective.

The goal of this project is to develop a School Knowledge Assistant that uses semantic search to understand the user's intent and retrieve the most relevant school-related information from a collection of documents.

🎯 Features
Persistent ChromaDB Database
Collection named school_documents
Stores 40+ school-related documents
Unique ID assigned to each document
Accepts natural language queries
Retrieves the Top 3 most relevant documents
Displays:
Document ID
Retrieved Document
Similarity Distance
Command Line Interface (CLI)
🛠 Technologies Used
Python
ChromaDB
Vector Database
Semantic Search
Natural Language Processing (NLP)
📂 Project Structure
Smart-Semantic-Search/
│
├── app.py
├── school_db/
├── README.md
└── requirements.txt
🔄 Workflow
Step 1

Install ChromaDB and the required Python libraries.

Step 2

Import the required libraries.

Step 3

Create a Persistent ChromaDB client.

Step 4

Create or access the school_documents collection.

Step 5

Prepare a list of school-related documents.

Step 6

Insert the documents into the database with unique IDs.

Step 7

Accept a natural language query from the user.

Step 8

Search the collection using semantic search.

Step 9

Display the top three most relevant documents along with their IDs and similarity scores.

💾 Database

Database Type:

Persistent ChromaDB

Collection Name:

school_documents

Database Folder:

school_db/
📚 Dataset

The dataset contains documents related to:

Admissions
School Timings
Attendance Policy
Library
Computer Lab
Science Lab
School Transport
Cafeteria
School Fees
Parent Teacher Meetings
School Rules
Uniform Policy
Mobile Phone Policy
Scholarships
Sports
Robotics Club
Annual Functions
Science Exhibitions
Environmental Club
Announcements
🔍 Sample Queries
What are the school timings?

How can I get admission?

Is transport available?

Can students use mobile phones?

When is the Parent Teacher Meeting?

What are the library timings?

When are the final examinations?

What documents are required for admission?

Does the school have a computer lab?

What extracurricular activities are available?
📊 Expected Output
Top 3 Relevant Documents

Document ID : DOC_07

Document :
School timings are from 8:00 AM to 2:00 PM from Monday to Friday.

Distance :
0.12
🎯 Learning Outcomes

After completing this project, students will be able to:

Understand semantic search.
Create a persistent vector database using ChromaDB.
Store and manage document embeddings.
Perform natural language document retrieval.
Build a simple AI-powered knowledge assistant.
🚀 Future Improvements
Add a graphical user interface (GUI)
Integrate with Streamlit
Connect to a PDF document loader
Support multiple schools
Add voice-based search
Build a chatbot interface
Integrate Large Language Models (LLMs)
👩‍💻 Author

Areesha Ali
