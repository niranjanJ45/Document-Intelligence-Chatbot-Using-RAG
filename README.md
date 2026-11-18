# Document Intelligence Chatbot Using RAG

A Streamlit app that lets you upload PDF documents and ask questions about
their contents. It uses OpenAI embeddings to index the uploaded documents and
a Groq-hosted language model to answer questions with retrieved context.

## Requirements

- Python 3.10 or newer
- An OpenAI API key for document embeddings
- A Groq API key for chat responses

## Setup (Windows PowerShell)

Run these commands from the repository root:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Create a `.env` file in the repository root:

```text
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
```

Keep `.env` private; it is excluded by `.gitignore`.

## Run

```powershell
python -m streamlit run .\apps\Pdf_Rag_agent.py
```

Upload one or more PDF files in the app. Uploaded files are saved locally in
`doc_files/`, which is excluded from Git.
