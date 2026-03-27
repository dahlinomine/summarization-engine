# Summarization Engine

![summarization](https://img.shields.io/badge/summarization-blue?style=flat-square) ![nlp](https://img.shields.io/badge/nlp-blue?style=flat-square) ![context](https://img.shields.io/badge/context-blue?style=flat-square)

A tool that compresses 100+ page documents into agent-readable hierarchical summaries.

## Overview
The Summarization Engine is a Python-based NLP utility designed to tackle the "lost in the middle" challenge of long-context documents. It transforms massive datasets and lengthy PDFs into structured, hierarchical summaries optimized for consumption by LLM agents and RAG (Retrieval-Augmented Generation) pipelines. By preserving semantic relationships across 100+ pages, it ensures critical context remains accessible even within constrained token windows.

## Features
*   **Hierarchical Compression:** Breaks down long-form text into nested summaries that preserve both high-level themes and granular details.
*   **Agent-Optimized Output:** Generates structured data formats specifically designed to improve the reasoning capabilities of downstream AI agents.
*   **Context Preservation:** Utilizes advanced chunking strategies to ensure document context is not lost during the summarization process.
*   **Large-Scale Processing:** Capable of handling 100+ page documents with efficient memory management and token usage.

## Installation
Ensure you have Python 3.8+ installed. Clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/username/summarization-engine.git
cd summarization-engine
pip install -r requirements.txt
```

## Usage
To process a document, run the `main.py` script with the path to your target file. You can specify output formats or compression levels via command-line arguments.

```bash
python main.py --input path/to/document.pdf --output summary.json
```

**Example:**
```python
from engine import Summarizer

# Initialize the engine
summarizer = Summarizer()

# Generate a hierarchical summary
summary = summarizer.compress("legal_brief_150_pages.pdf")
print(summary.hierarchy_root)
```

## Contributing
We welcome contributions to improve the engine's efficiency and accuracy. Please fork the repository, create a feature branch, and submit a pull request with a detailed description of your changes. Ensure all tests pass before submission.

## License
This project is licensed under the [MIT License](LICENSE).