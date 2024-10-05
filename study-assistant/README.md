# PDF Chat Assistant Application

This project implements a PDF-based chat assistant using **Spring Boot**, **Langchain 4J**, and **Astra DB**. The application allows users to query PDF documents and receive human-readable responses powered by large language models (LLMs) like **OpenAI GPT-3/4**.

## Features

- **PDF Document Ingestion:** Reads and processes PDF files, splitting text into smaller segments for efficient handling.
- **Embedding Generation:** Converts text segments into numeric embeddings using OpenAI GPT-3/4 or all-MiniLM-L6-v2 models.
- **Semantic Search:** Stores and retrieves embeddings in **Astra DB** for fast, vector-based search functionality.
- **LLM Integration:** Uses OpenAI’s API to generate human-readable responses from embeddings, providing contextual answers to user queries.

## Architecture

1. **PDF Ingestion and Splitting**: 
   - PDF files are split into manageable text segments using the **Document Splitter** from Langchain 4J.
2. **Embedding Creation**:
   - Text segments are transformed into embeddings (numeric vectors) using the LLM embedding models like **GPT-3/4** or **all-MiniLM-L6-v2**.
3. **Storage**:
   - Embeddings are stored in **Astra DB**, a vector-based NoSQL database, for efficient retrieval and semantic search.
4. **Query Processing**:
   - User queries are converted to embeddings and matched against the stored PDF embeddings in **Astra DB**.
5. **Response Generation**:
   - Matched embeddings are processed by OpenAI’s GPT-3/4 to return natural, human-readable responses to users.

## Getting Started

### Prerequisites

- Java 21+
- OpenAI API Key
- Astra DB account
- IntelliJ IDEA (or any other Java IDE)

### Setup

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-repo/langchain4j-pdf-assistant.git
    cd langchain4j-pdf-assistant
    ```

2. **Configure OpenAI API Key**:
   - Create an account on [OpenAI](https://beta.openai.com/) and generate an API key.
   - Add your API​⬤