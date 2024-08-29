# Retrieval-Augmented Generation (RAG) Application

## Introduction

This RAG Application is a Python-based tool that combines document retrieval and text generation to answer questions based on the content of various document types (PDF, DOCX, TXT). It uses OpenAI's API for text embedding and generation, providing context-aware responses to user queries.

## Features

- Support for multiple document types (PDF, DOCX, TXT)
- Text preprocessing and chunking for efficient processing
- Semantic search using OpenAI's text embeddings
- Context-aware response generation using GPT-3.5-turbo
- Easy-to-use interface for asking questions about document content

## Prerequisites
Before you begin, ensure you have met the following requirements:

- Python 3.7 or higher
- An OpenAI API key


## Installation
To run this project, you need to install the required libraries. Use the following command:

```bash
pip install pymupdf python-docx openai==0.28 numpy
```
## Setting Up the OpenAI API Key
Create a .env file in the project directory.
Add your OpenAI API key to the .env file:
```bash
OPENAI_API_KEY=your_openai_api_key_here
```

## Usage
### 1. Load the Code
Ensure the code provided in this repository is saved in a Python script (rag_application.py).

### 2. Update the File Path
Update the file_path variable in the script to point to the document you want to process:

```python
file_path = "path_to_your_file.pdf"  # Update this path
```

### 3. Run the Application
Run the Python script to test the RAG application. You can query the document using the rag_generate() function. For example:

```python
prompt = "What is the subject of this text?"
response = rag_generate(prompt)
print(response)
```

### 4. Query Examples
You can try querying with different prompts:

```python
prompts = ["What is NLP?", "How does machine learning work?", "What is deep learning?"]

for prompt in prompts:
    response = rag_generate(prompt)
    print(response)
```

## Customization

- Adjust the chunk_size in the chunk_text function to change how the document is split.
- Modify the similarity_threshold in the rag_application function to control how closely the context must match the query.
- Change the max_tokens and temperature parameters in the generate_response function to adjust the length and creativity of the generated responses.

## Limitations

- The application currently only supports `.txt`, `.docx`, and `.pdf` files.
- The similarity threshold for generating responses is set at 0.5, which might need tuning based on different use cases.
- The application requires an active OpenAI API key, which may incur costs.
