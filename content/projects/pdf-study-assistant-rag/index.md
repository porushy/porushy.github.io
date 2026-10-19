---
title: 'PDF Study Assistant: Retrieval-Augmented Generation (RAG)'
summary: An end-to-end RAG pipeline over a 193-page government report that answers with exact page-level citations, refuses out-of-domain queries, and uses hybrid dense + BM25 retrieval.
date: 2026-10-15
featured: true
links:
  - type: code
    url: https://github.com/porushy/RAG
    label: Code
    icon: brands/github
tags:
  - Generative AI
  - NLP
  - RAG
  - LLMs
---

Oct 2026

Python · LangChain (LCEL) · FAISS · Sentence-Transformers · BM25 · FastAPI · LLM APIs (Gemini/Groq)

- Engineered an end-to-end RAG pipeline to query a complex 193-page government report. The system delivers exact page-level citations for grounded answers and strictly refuses out-of-domain queries. The pipeline features custom text cleaning, page-aware chunking, local MiniLM embeddings, and a FAISS vector index.
- Built a custom evaluation harness using 20 gold-labeled queries to optimize chunk sizes and retrieval k. Achieved 100% top-3 retrieval for factual queries and 93% (14/15) generation accuracy, successfully tracing the single error to an upstream text-cleaning defect.
- Optimized retrieval performance by implementing a hybrid search strategy (dense + BM25). This outperformed doubling the dense results, boosting multi-page answer coverage from 42% to 73% and correct citation rates from 32% to 53%.
- Documented architectural failure modes (multi-hop, aggregate, and table queries) and engineered system robustness via exponential backoff for rate limits, automatic model fallback, and strict output citation verification.
- Deployed a chat-style FastAPI web app featuring dynamic model and search selection, session history management, and interactive citations that directly open the source PDF to the exact referenced page.

<!--more-->
