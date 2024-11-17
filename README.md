
# Document Intelligence with RAG, Hybrid Search, and Reranking

This repository provides a pipeline for processing documents and applying Retrieval-Augmented Generation (RAG) enhanced with Hybrid Search and Reranking to improve response accuracy. Using Azure Document Intelligence, this tool converts various document types (e.g., PDF, Excel) into `.txt` format, facilitating downstream RAG processes with precise retrieval.

## Features

- **Document Conversion**: Converts PDF, Excel, and other document types into plain text for analysis.
- **Hybrid Search**: Combines BM25 keyword-based and FAISS vector-based retrieval for both exact matches and semantic relevance.
- **Reranking**: Uses a cross-encoder model to rerank results for optimal relevance, ensuring accurate responses to user queries.
- **Flexible Querying**: Processes natural language queries and retrieves contextually relevant content from stored documents.

## Requirements

To install the necessary dependencies, use the provided requirements.txt file:

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

## Usage

### Step 1: Document Processing

1. Place your PDF and Excel files in the designated directory.
2. Run the document processing script to convert each document into `.txt` format.

### Step 2: Query Execution with RAG, Hybrid Search, and Reranking

After documents are processed, use the RAG pipeline with Hybrid Search and Reranking to retrieve accurate responses.

### Running the Jupyter Notebook

To use the provided Jupyter notebook, open the file in your preferred notebook environment and execute each cell in sequence to preprocess documents and query the RAG pipeline with Hybrid Search and Reranking.

## Output

- **Generated Responses**: Outputs contextually accurate answers to user queries.
- **Processed Files**: Stores converted `.txt` files in the directory, ready for analysis or RAG processing.
- **nke-10k-2023.txt**: The txt file generated through this process contains plain text extracted from first ten pages of the PDF document . This file is stored in the designated directory and is ready for analysis or integration into RAG workflows. It provides easily accessible text data that simplifies downstream tasks like search, retrieval, and question-answering.
## License

This project is licensed under the MIT License.
