# PDF Query with LangChain

This repository provides an implementation for querying information from PDF documents using LangChain, OpenAI embeddings, and vector databases such as Cassandra DB/Astra DB. The system is designed to split a PDF document into text chunks, create embeddings for each chunk, and store them in a vector database for efficient similarity searches based on user queries.

## Features

- **PDF Parsing**: Reads and splits a PDF document into manageable text chunks.
- **Text Embeddings**: Utilizes OpenAI embeddings to encode text chunks into high-dimensional vectors.
- **Vector Database Integration**: Stores embeddings in a vector database for fast and accurate similarity search.
- **Query Handling**: Allows users to input natural language queries to retrieve relevant information from the document.
- **Powered by LangChain**: Efficiently handles document chunking and query processes.

## Workflow

1. **PDF Upload**: A PDF document is uploaded for processing.
2. **Document Chunking**: The PDF is read and split into smaller text chunks.
3. **Text Embedding Creation**: Each text chunk is converted into an embedding using OpenAI's embeddings.
4. **Storage in Vector Database**: The embeddings are stored in a vector database (e.g., Cassandra DB or Astra DB).
5. **Querying**:
   - A user inputs a text query.
   - The system creates an embedding for the query.
   - The vector database performs a similarity search to find the most relevant text chunks.
6. **Results Retrieval**: Relevant chunks are returned as the result of the query.

## Architecture Overview

![image](https://github.com/user-attachments/assets/6bb0ab35-0da9-4ec8-9685-06a985cb3043)


The diagram outlines the workflow:
- PDF documents are processed into text chunks.
- OpenAI embeddings are generated for these chunks.
- Embeddings are stored in a vector database for querying.
- User queries are converted into embeddings and matched with stored embeddings for similarity search.

## Technologies Used

- **[LangChain](https://www.langchain.com/)**: For managing document chunking and query workflows.
- **[OpenAI API](https://platform.openai.com/docs/)**: For generating text embeddings.
- **[Cassandra DB/Astra DB](https://www.datastax.com/products/datastax-astra/)**: As the vector database backend for storing and retrieving embeddings.
- **Python**: Core programming language for implementation.

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- OpenAI API key
- Astra DB account for vector database setup

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/pdf-query-langchain.git
   cd pdf-query-langchain

2. Install dependencies:
 ```bash
pip install -r requirements.txt

3. Set up environment variables:
Create a .env file in the root directory and add the following:
OPENAI_API_KEY=your_openai_api_key
ASTRA_DB_APPLICATION_TOKEN=your_astra_db_token

4. Start the application:
python app.py
