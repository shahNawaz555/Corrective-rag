# Corrective RAG

This repository implements a **Retrieval-Augmented Generation (RAG)** pipeline that enhances the question-answering process through document retrieval, relevance grading, question re-writing, and web search integration. The system is built using **LangChain**, **Google Generative AI**, **Tavily**, **Chroma**, and **GROQ** to create an optimized, structured workflow for efficient information retrieval and answer generation.

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Setup](#setup)
5. [Usage](#usage)
6. [Pipeline Overview](#pipeline-overview)
7. [License](#license)

## Introduction

**Corrective RAG** is a dynamic framework for improving the quality of answers by combining document retrieval, relevance grading, question transformation, and web search enhancements. It uses **LangChain**, integrated with various APIs and tools, to process and refine queries through an optimized flow.

The pipeline incorporates several key tasks:
- **Document Retrieval** using **Chroma** for efficient vector storage.
- **Relevance Grading** to filter out irrelevant documents.
- **Question Re-writing** to better align with web search.
- **Web Search Integration** to improve context.
- **Answer Generation** using **Google Generative AI**.

## Features
- **Document Retrieval**: Retrieves relevant documents from predefined URLs.
- **Relevance Grading**: Evaluates the relevance of each retrieved document.
- **Question Re-writing**: Transforms the input question for better web search results.
- **Web Search Integration**: Performs web searches for additional context.
- **Answer Generation**: Combines relevant documents to generate answers.

## Requirements

To run the project, you need the following:

- Python 3.7 or higher
- Dependencies from `requirements.txt`
- API keys for the following services:
  - **Google Generative AI**
  - **Tavily Search**
  - **GROQ**
  - **LangChain**

## Setup

### 1. Clone the Repository

git clone https://github.com/your-username/corrective-rag.git
cd corrective-rag
Pipeline Overview
The Corrective RAG pipeline follows a sequence of tasks to optimize the question-answering process:

Document Retrieval: Load documents from URLs and split them into smaller chunks.

Relevance Grading: Evaluate the relevance of documents to the user’s question.

Generation: Generate an answer based on the relevant documents using RAG.

Web Search: Enhance the context of the answer by performing web searches when necessary.

Question Rewriting: Re-write the input question for better web search results.

Workflow Details
The pipeline consists of several nodes:

Retrieve: Retrieve documents relevant to the question.

Grade Documents: Grade the relevance of retrieved documents.

Generate: Generate answers using RAG.

Transform Query: Rephrase the question for better clarity.

Web Search: Enhance context by adding web search results.

A StateGraph manages the flow of tasks, ensuring each step is processed in order.

