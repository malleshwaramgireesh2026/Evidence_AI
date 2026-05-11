 
# EvidenceFlow AI
 
EvidenceFlow AI is a Streamlit-based multi-document RAG platform for source-grounded question answering, document comparison, citation tracing, answer evaluation, hallucination guardrails, and downloadable chat history.
 
It lets users upload documents, build a searchable FAISS vector index, ask questions from uploaded files, compare evidence across documents, inspect retrieved sources, evaluate answer quality, and export the full evidence trail.
 
## Application Preview
 
<img src="assets/evidenceflow-ui.png" alt="EvidenceFlow AI application preview" width="900">
 
## Project Highlight
 
**EvidenceFlow AI: Multi-Document RAG Platform with Source-Grounded Evaluation**
 
EvidenceFlow AI is a multi-document RAG platform built with LangChain, FAISS, HuggingFace embeddings, Groq LLaMA, and Streamlit. It supports workspace-based document upload, source-grounded question answering, cross-document comparison, follow-up memory, relevance-scored citations, answer evaluation, hallucination guardrails, and exportable chat histories.
 
## Features
 
- Multi-document upload with PDF, TXT, and MD support

- Workspace-based document organization

- FAISS vector indexing for semantic search

- Source-grounded question answering

- Cross-document comparison reports

- Follow-up question memory using recent chat history

- Exact source citations with document name, page number, and relevance score

- Answer evaluation using grounding, relevance, citation, and completeness metrics

- Hallucination guardrails for low-confidence or missing-citation answers

- Downloadable chat history as an evidence trail

- Clean Streamlit tab-based interface
 
## Tech Stack
 
- Python

- Streamlit

- LangChain

- FAISS

- HuggingFace Embeddings

- Groq API

- LLaMA 3.1

- PyPDF
 
## Project Architecture
 
```text

User Uploads Documents

        |

        v

Document Loader

        |

        v

Text Chunking

        |

        v

HuggingFace Embeddings

        |

        v

FAISS Vector Index

        |

        v

Semantic Retrieval

        |

        v

Groq LLaMA Response Generation

        |

        v

Answer + Citations + Evaluation
```


