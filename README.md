# PDF Question-Answering System

A Python application that creates an interactive Q&A system for PDF documents using LangChain, FAISS, and Ollama.

## Features

- PDF document loading and parsing
- Text chunking with overlap for context preservation
- Vector embeddings using Ollama's LLaMA2
- Efficient similarity search with FAISS
- Interactive Q&A interface

## Prerequisites

- Python 3.x
- Ollama with LLaMA2 model installed
- Required Python packages:
  - langchain
  - langchain-community
  - langchain-ollama
  - python-dotenv
  - faiss-cpu
  - pypdf

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Mohamed-AH/langchainchat.git
cd langchainchat
```

2. Install dependencies:
```bash
pip install langchain langchain-community langchain-ollama python-dotenv faiss-cpu pypdf
```

3. Install Ollama and download the LLaMA2 model:
```bash
# Follow Ollama installation instructions at https://ollama.ai
ollama pull llama2
```

## Usage

1. Place your PDF file in the project directory

2. Run the application:
```bash
python main.py
```

3. Enter questions when prompted. Type 'exit' to quit.

## How It Works

1. The system loads and splits the PDF into manageable chunks
2. Text chunks are converted to vector embeddings using LLaMA2
3. FAISS creates a searchable vector store
4. User questions are processed to find relevant text chunks
5. LLaMA2 generates answers based on the retrieved context

## Project Structure

```
└── langchainchat/
    ├── main.py          # Main application code
    ├── .env            # Environment variables (create this)
    └── README.md       # Documentation
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

## License

[MIT](https://choosealicense.com/licenses/mit/)
