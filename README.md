 
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

## How It Works
 
1. The user creates or selects a workspace.

2. The user uploads one or more documents.

3. Documents are loaded and split into chunks.

4. Each chunk is converted into embeddings using HuggingFace embeddings.

5. FAISS stores the vector index for semantic retrieval.

6. The user asks a question or requests document comparison.

7. Relevant chunks are retrieved from the vector index.

8. Groq LLaMA generates an answer using only the retrieved context.

9. The app displays the answer, source citations, relevance scores, and evaluation metrics.

10. The user can download the chat history as an evidence trail.
 
## Evaluation Metrics
 
EvidenceFlow AI includes lightweight answer evaluation:
 
- **Grounding**: Checks whether answer terms appear in retrieved source context.

- **Relevance**: Checks whether important question terms appear in the generated answer.

- **Citation**: Checks whether the answer includes document/page/source references.

- **Completeness**: Checks whether the answer has enough detail.

- **Overall Score**: Combined score from grounding, relevance, citation, and completeness.
 
These metrics are practical guardrails for a demo system and are not a replacement for full human evaluation.
 
## Hallucination Guardrails
 
The assistant is instructed to:
 
- Answer only from uploaded document context

- Say `Insufficient information in provided documents` when evidence is missing

- Avoid inventing facts, dates, numbers, policies, or conclusions

- Warn users when an answer has low confidence

- Warn users when citations may be missing
 
## Example Use Cases
 
- Research paper analysis

- Medical guideline Q&A

- Legal document comparison

- Policy document search

- Business report summarization

- Study note generation

- Contract or compliance review
 
## Setup
 
Clone the repository:
 
```bash

git clone https://github.com/YOUR_USERNAME/evidenceflow-ai.git

cd evidenceflow-ai

 
 
 
 
