# Retrieval-Augmented Generation (RAG) Application

## Description
This project demonstrates a Retrieval-Augmented Generation (RAG) application using OpenAI's GPT-3.5 Turbo model. The application allows users to query text data from various file formats (TXT, DOCX, PDF) and generates relevant responses based on the content retrieved from the files. The project utilizes OpenAI's text embeddings to vectorize the text and calculate the similarity between the user's query and the content of the files. If relevant information is found, the model generates a response based on the retrieved text.

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

## Notes
Ensure that your OpenAI API key is valid and active.
The similarity threshold is set to 0.5. Adjust it if necessary to refine the relevance of retrieved information.
This application is designed to work with small to medium-sized text documents. Performance on large files may vary.

## Limitations

- The application currently only supports `.txt`, `.docx`, and `.pdf` files.
- The similarity threshold for generating responses is set at 0.5, which might need tuning based on different use cases.
- The application requires an active OpenAI API key, which may incur costs.

