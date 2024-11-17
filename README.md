
# Document Intelligence with RAG, Hybrid Search, and Reranking

This repository provides a solution for document processing and retrieval tasks by implementing a pipeline that combines Azure Document Intelligence and Retrieval-Augmented Generation (RAG) techniques. The addition of Hybrid Search and Reranking methods improves the accuracy and relevance of responses to natural language queries.

## What We Did

1. **Document Conversion**: Used Azure Document Intelligence to convert documents in PDF and Excel formats into `.txt` files. This preprocessing step makes documents easier to process and enhances their accessibility for information retrieval tasks.
2. **Hybrid Search and Reranking**: Implemented Hybrid Search with BM25 and FAISS vector retrieval to combine the advantages of keyword-based and semantic search. Additionally, a cross-encoder reranker was used to refine and prioritize the retrieved documents.
3. **RAG Pipeline**: Applied a RAG pipeline to enhance response quality by utilizing both retrieved document content and generation capabilities.

## What We Learned

Throughout this project, we learned that:
- **Azure Document Intelligence** effectively extracts structured data from PDF and Excel files, which can then be used for retrieval tasks.
- **Combining Retrieval Techniques** improves relevance; while BM25 excels at keyword-based matching, FAISS and reranking with cross-encoders significantly improve semantic accuracy.
- **Hybrid Search with Reranking** allows for a balance between speed and accuracy, which is essential for real-time applications.

## Results

- **Enhanced Document Accessibility**: Documents are now available in a `.txt` format that is straightforward for text-based search and processing tasks.
- **Improved Retrieval Accuracy**: By using Hybrid Search and Reranking, this pipeline provides more accurate answers to user queries, especially in complex or ambiguous cases.
- **Flexible Querying and Response Generation**: The combined use of RAG, Hybrid Search, and Reranking allows the system to retrieve and generate contextually accurate responses.

## Features

- **Document Conversion**: Converts PDF, Excel, and other document types into plain text for analysis.
- **Hybrid Search**: Combines BM25 keyword-based and FAISS vector-based retrieval for both exact matches and semantic relevance.
- **Reranking**: Uses a cross-encoder model to rerank results for optimal relevance, ensuring accurate responses to user queries.
- **Flexible Querying**: Processes natural language queries and retrieves contextually relevant content from stored documents.

## Requirements

To install the necessary dependencies, use the provided `requirements.txt` file:

```bash
pip install -r requirements.txt
```

## Azure Setup

1. **Azure Document Intelligence**: Set up an Azure Document Intelligence instance, obtaining your endpoint and API key.
2. **Environment Variables**: Configure your Azure endpoint and API key in environment variables or directly in the code.

## Pipeline Overview

1. **Document Ingestion and Conversion**: Converts documents (PDF, Excel) to `.txt` files using Azure Document Intelligence, preparing them for RAG.
2. **Hybrid Search**: Utilizes both BM25 for keyword search and FAISS for vector similarity, allowing for comprehensive document retrieval.
3. **Reranking**: Applies a cross-encoder model to rerank retrieved documents based on relevance.
4. **Retrieval-Augmented Generation (RAG)**: Answers queries accurately by combining retrieval and generation capabilities.

## Converted Text Files

The `txt` files generated through this process contain plain text extracted from the original PDF or Excel documents. These files are stored in the designated directory and are ready for analysis or integration into RAG workflows. They provide easily accessible text data that simplifies downstream tasks like search, retrieval, and question-answering.

## Output

- **Generated Responses**: Outputs contextually accurate answers to user queries.
- **Processed Files**: Stores converted `.txt` files in the directory, ready for analysis or RAG processing.
