AI Contract Compliance Checker
A LangChain-based RAG (Retrieval-Augmented Generation) system that evaluates contract documents against 29 predefined compliance rules using Groq LLM and vector similarity search.
 Project Overview
This system automatically analyzes legal contracts and generates compliance reports by:

Ingesting PDF, TXT, and DOCX contract documents
Performing keyword-based rule matching
Using semantic search with ChromaDB vector store
Leveraging Groq's Llama 3.3 70B model for intelligent analysis
Generating detailed compliance reports with evidence

Dataset
CUAD (Contract Understanding Atticus Dataset)

Source: https://www.atticusprojectai.org/cuad
510 commercial legal contracts
13,000+ expert annotations
Covers 41 contract clause types

Technologies Used

LangChain: Framework for LLM applications
Groq: Fast LLM inference with Llama 3.3 70B
ChromaDB: Vector database for semantic search
HuggingFace: Sentence transformers for embeddings
Streamlit: Web application interface
PyPDF2, python-docx: Document parsing


Compliance Rules (29 Total)
HIGH Severity (12 rules)

Confidentiality/NDA clauses
Termination conditions
Liability limitations
Governing law
Payment terms
Data protection
Intellectual property
Termination for cause
Confidentiality duration
Limitation of damages
Compliance with laws
Performance standards

MEDIUM Severity (15 rules)

Indemnification, Warranty, Dispute resolution, Renewal terms, Insurance, Modification, Audit rights, Insurance requirements, Severability, Assignment restriction, Notice requirements, Entire agreement, Export control, Subcontracting, Insurance coverage

LOW Severity (2 rules)

Force majeure, Counterparts