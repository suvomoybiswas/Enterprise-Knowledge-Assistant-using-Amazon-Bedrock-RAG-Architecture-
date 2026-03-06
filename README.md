# Enterprise-Knowledge-Assistant-using-Amazon-Bedrock-RAG-Architecture-
Enterprise Knowledge Assistant is built with Amazon Bedrock, OpenSearch Serverless, and S3 using Retrieval Augmented Generation (RAG) architecture.
📌 Project Overview

This project demonstrates how to build an Enterprise Knowledge Assistant using Retrieval Augmented Generation (RAG) architecture with Amazon Bedrock, Amazon S3, and Amazon OpenSearch Serverless.

The system enables users to query enterprise documents using natural language, retrieving relevant information from internal documents and generating intelligent responses using foundation models.

Instead of relying only on pre-trained model knowledge, the assistant retrieves real enterprise data and uses it as context for generating accurate responses.

🧠 Key Features

✔ Build a Generative AI knowledge assistant
✔ Implement Retrieval Augmented Generation (RAG)
✔ Store enterprise documents in Amazon S3
✔ Convert documents into vector embeddings
✔ Store embeddings in OpenSearch Serverless
✔ Perform a semantic search for relevant information
✔ Generate responses using Amazon Bedrock foundation models

🏗 Architecture




Architecture Flow

1️⃣ Upload enterprise documents to Amazon S3

2️⃣ Configure Amazon Bedrock Knowledge Base

3️⃣ Documents are split into text chunks

4️⃣ Chunks are converted into vector embeddings

5️⃣ Embeddings are stored in Amazon OpenSearch Serverless

6️⃣ User submits a natural language query

7️⃣ Relevant document chunks are retrieved using vector similarity search

8️⃣ Amazon Bedrock foundation model generates the final response

🧰 AWS Services Used
☁️ Amazon S3

Object storage used to store enterprise documents.

Features:

Highly scalable storage

Stores files as objects in buckets

Maximum object size: 5 TB

🤖 Amazon Bedrock

Fully managed service that provides access to foundation models (FMs).

Used in this project for:

Creating the Knowledge Base

Generating embeddings

Producing AI responses from queries

Models used:

Amazon Titan Embeddings

Amazon Nova Lite

🔎 Amazon OpenSearch Serverless

OpenSearch Serverless acts as the vector database.

Responsibilities:

Store vector embeddings

Perform similarity search

Retrieve relevant document chunks

Supported vector similarity metrics:

Cosine similarity

Euclidean distance

Dot product

📚 Core AI Concepts Implemented
Vector Embeddings

Embeddings convert text into numerical vectors that represent semantic meaning.

Example:


"Increase quarterly revenue"

→ vector representation



This allows the system to perform semantic similarity search instead of keyword search.

Retrieval Augmented Generation (RAG)

RAG combines:


Information Retrieval + Large Language Models



Workflow:

User query → converted into vector

Vector database retrieves relevant document chunks

Retrieved content is passed to the LLM

LLM generates a contextual answer

Benefits:

More accurate responses

Reduced hallucination

Ability to use proprietary enterprise data

📂 Project Structure

aws-bedrock-enterprise-knowledge-assistant
│
├── README.md
│
├── architecture
│   └── architecture-diagram.png
│
├── documentation
│   ├── project-overview.md
│   ├── aws-services-used.md
│   └── rag-explained.md
│
├── guide
│   └── step-by-step-lab-guide.md
│
├── metadata
│   └── metadata-example.json
│
├── lab-files
│   ├── sales-details.csv
│   └── sales-report.pdf
│
└── screenshots
    ├── 01-s3-bucket.png
    ├── 02-bedrock-model-enabled.png
    ├── 03-knowledge-base-created.png
    ├── 04-opensearch-vector-store.png
    ├── 05-data-source-sync.png
    └── 06-query-test.png


⚙ Implementation Steps
Step 1 — Upload Documents

Upload enterprise documents to Amazon S3 buckets

Example:


sales-data
sales-reports


Step 2 — Enable Bedrock Models

Enable foundation models in the Amazon Bedrock console

Models used:

Amazon Titan Embeddings

Amazon Nova Lite

Step 3 — Create Knowledge Base

Create a Bedrock Knowledge Base named:


Sales KB


Step 4 — Configure Vector Store

Configure Amazon OpenSearch Serverless as the vector store.

Collection type:


Vector Search


Step 5 — Add Data Sources

Add two data sources to the knowledge base:

Data Source	Description
sales-data	Sales CSV data
sales-reports	Sales report PDF
Step 6 — Sync Data Sources

During synchronization:

Documents are processed

Text is chunked

Embeddings are generated

Embeddings are stored in OpenSearch

Step 7 — Test Knowledge Base

Example query:


How can the sales team improve performance?



The system retrieves relevant document chunks and generates a contextual response.

🧪 Validation Criteria

The project validation checks:

✔ A Bedrock Knowledge Base named Sales KB exists
✔ Two data sources are configured
✔ Both data sources are successfully synced
✔ Documents are ingested into the vector store

📸 Screenshots

Screenshots included in /screenshots folder:

S3 bucket setup

Bedrock model enablement

Knowledge base configuration

OpenSearch vector store

Data source sync

Query test results

🎯 Learning Outcomes

This project demonstrates:

✔ Generative AI application architecture
✔ Vector databases and semantic search
✔ Retrieval Augmented Generation (RAG)
✔ Integration of enterprise data with LLMs
✔ Building AI knowledge assistants using AWS

🚀 Future Improvements

Potential enhancements:

Build a chatbot interface

Integrate with Slack / Microsoft Teams

Automate the document ingestion pipeline

Deploy using AWS Lambda + API Gateway

Add real-time knowledge updates

👨‍💻 Author

Cloud & AI Enthusiast

Focused on:

Cloud Computing ☁️

Generative AI 🤖

Machine Learning 📊

AWS Architecture 🏗
