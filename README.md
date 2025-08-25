## Setup & Installation

### Voraussetzungen
- Python 3.13+
- Docker (für Neo4j)
- OpenAI API Key (optional)

### Installation
```bash
git clone <repository-url>
cd rag-benchmark

# Virtual Environment
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# Dependencies
pip install -e .

# Zusätzliche Downloads
python -m spacy download de_core_news_sm
python -c "import nltk; nltk.download('punkt')"

````

### Ausführung
Die Notebooks müssen in Reihenfolge ausgeführt werden:

- 01_setup_and_data.ipynb - Datenaufbereitung
- 02_vector_retrieval.ipynb - FAISS Vector Retrieval
- 03_graph_retrieval.ipynb - Neo4j Graph Retrieval
- 04_llm_integration.ipynb - LLM Integration & RAG
- 05_evaluation.ipynb - BLEU/ROUGE Evaluation
- 06_summary.ipynb - Zusammenfassung & Report

### Technische Details

- LLM: GPT-4.1-nano via OpenAI API
- Embeddings: paraphrase-multilingual-MiniLM-L12-v2
- Evaluation: BLEU, ROUGE, Success Rate
- Korpus: 15 FAQ-Dokumente zu RAG/AI-Themen

### Autor
Lukas Schaumlöffel - Master Informatik (HAW Hamburg)