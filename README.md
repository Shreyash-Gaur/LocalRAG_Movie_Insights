# Self-RAG Movie Explorer

This repository demonstrates a **Self-Retrieval Augmented Generation (Self-RAG)** pipeline for querying and generating insights from a movie database. The project uses **LangGraph** for flow management, **Pinecone** for vector-based retrieval, and **LLaMA 3.2** as the local language model for generation. Self-RAG incorporates self-reflection and grading mechanisms to improve the accuracy and relevance of retrieved content.

---

## Project Overview

- **Objective:** Build a pipeline to retrieve relevant movie data and generate structured insights with enhanced accuracy using self-evaluation mechanisms.
- **Key Components:**
  - **LangGraph:** Manages the pipeline workflow and logic.
  - **Pinecone:** Serves as the vector database for fast and scalable retrieval.
  - **LLaMA 3.2:** Provides local language model capabilities for response generation.
  - **Self-Grading Mechanism:** Evaluates and refines retrieved content for improved accuracy.

---

## Features

- **Local Model Integration:**
  Utilizes the LLaMA 3.2 model for generating responses, eliminating reliance on external APIs.

- **Efficient Retrieval:**
  Employs Pinecone's vector database and embeddings to query a sample movie dataset efficiently.

- **Self-Reflection:**
  Implements a self-grading mechanism that scores and refines retrieval and generation outputs for better results.

- **Structured Outputs:**
  Generates well-structured, human-readable responses from the retrieved movie data.

---

## Workflow Overview

1. **Embedding Creation:**
   Leverages a local embedding model (e.g., `sentence-transformers/all-MiniLM-L6-v2`) to convert movie metadata into vector representations.

2. **Vector Search:**
   Queries the Pinecone vector store using similarity search to retrieve relevant documents.

3. **Response Generation:**
   Generates responses using the LLaMA 3.2 language model, incorporating retrieved data.

4. **Self-Grading:**
   Applies a grading mechanism to evaluate and refine the output, ensuring high relevance and quality.

---

## Example Use Case

### Query:
"Tell me about movies directed by James Cameron."

### Output:
1. **Title:** Titanic  
   **Description:** A romance set against the ill-fated voyage of the RMS Titanic.

2. **Title:** Avatar  
   **Description:** A visually stunning story set on the alien world of Pandora.

---

## Technologies Used

- **LangChain and LangGraph**
- **Pinecone Vector Database**
- **LLaMA 3.2 Local Language Model**
- **Transformers Library**
- **Sentence Transformers for Embeddings**

---

## Acknowledgments

- **Meta AI:** For the LLaMA 3.2 model.
- **Pinecone:** For their scalable and efficient vector database.
- **LangChain:** For providing powerful tools for RAG pipelines.

