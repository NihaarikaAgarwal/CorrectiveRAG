# CRAG: Corrective Retrieval-Augmented Generation with LangGraph

Even though supported with RAG, LLMs can sometimes lead to outdated or low quality retrieveal, giving wrong answers, low quality of response or hallucinating. This workflow is inspitred from the paper: Corrective retrieval augmented generation (CRAG) (https://arxiv.org/abs/2401.15884). It uses the LLM to answer if the docs are relevant to the question and if not it repharses the query and searches web for more context. This repository demonstrates the implementation of an **Agentic Corrective RAG (CRAG) System** using **LangGraph**. The notebook guides through building a self-correcting Retrieval-Augmented Generation pipeline, where the LLM assesses and refines its own responses using document grading and query rewriting.

## Overview

Corrective RAG (CRAG) is a retrieval-augmented generation system enhanced with:
- **Document grading** to filter irrelevant documents
- **Query rewriting** to improve subsequent retrieval
- **LangGraph** orchestration to implement feedback loops

This system enables more accurate and robust question-answering capabilities by **self-correcting based on retrieval feedback**.

## Features

-  Initial document retrieval using vector search
-  Relevance scoring of retrieved documents using a Pydantic LLM Grader
-  Query rewriting if retrieved documents are irrelevant
-  Final answer generation with refined documents
-  Built using LangGraph, LangChain, and HuggingFace models

LLM: Mistral-7B-Instruct-v0.1
VectorDB: ChromaDB

## References
Shi-Qi Yan, Jia-Chen Gu, Yun Zhu, Zhen-Hua Ling. (2024). Corrective Retrieval Augmented Generation. arXiv:2401.15884. https://arxiv.org/abs/2401.15884

