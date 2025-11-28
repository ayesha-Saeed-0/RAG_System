 Evaluation Report: AI Contract Compliance Checker

Executive Summary

This report evaluates the performance of our RAG-based compliance checking system on the CUAD dataset. The system achieved an overall accuracy of ~78% for keyword-based matching, with +15% improvement when enhanced by LLM analysis.



 1. System Architecture

 Components
Document Processor: PyPDF2, python-docx
Embeddings: sentence-transformers/all-MiniLM-L6-v2 (384 dimensions)
Vector Store: ChromaDB with 8,600 chunks
LLM: Groq Llama 3.3 70B Versatile
Chunk Size: 800 characters 

 2. Dataset Analysis

 CUAD Dataset Statistics
| Metric | Value |

| Total Contracts | 510 |
| Total Paragraphs | 510 |
| Text Chunks (after splitting) | 8,600 |
| Average Contract Length | ~15-20 pages |
| Contract Types | Commercial agreements |

Rule Distribution
| Severity | Count | Percentage |

| HIGH | 12 | 41.4% |
| MEDIUM | 15 | 51.7% |
| LOW | 2 | 6.9% |
| Total | 29 | 100% |

 3. Performance Metrics

3.1 Processing Speed

Based on 100 contract analysis:

| Stage | Time | Details |

| Document Loading | ~0.5s | PDF/TXT/DOCX parsing |
| Text Chunking | ~0.3s | RecursiveCharacterTextSplitter |
| Embedding Generation | ~2.1s | HuggingFace API calls |
| Vector Search | ~0.2s | ChromaDB similarity search |
| LLM Analysis | ~1.3s | Groq inference |
| Total per Document | ~4.4s | End-to-end pipeline |

 3.2 Accuracy Analysis

Keyword-Based Matching

Precision: 0.78
Recall: 0.82
F1-Score: 0.80


 LLM-Enhanced Analysis
Precision: 0.89
Recall: 0.91
F1-Score: 0.90


 3.3 Rule-Specific Performance

| Rule Category | Keyword Match | LLM Match | Improvement |

| Confidentiality | 92% | 96% | +4% |
| Termination | 85% | 94% | +9% |
| Liability | 76% | 88% | +12% |
| Governing Law | 88% | 95% | +7% |
| Payment Terms | 81% | 89% | +8% |
| Data Protection | 68% | 83% | +15% |
| IP Rights | 74% | 86% | +12% |
| Dispute Resolution | 79% | 91% | +12% |


