# Reducing Hallucinations in RPG Session Support Systems with RAG

## Plan

### 1. Corpus & Baseline
- Corpus assembly (core rulebook, what else?)
- Create and annotate baseline queries
### 2. RAG Implementation
- PDF extraction
- Chunking strategy
- Embedding
### 3. Retriever
- Vector DB
- Retrieval strategy
### 4. Content generation with retrieved context
- Model selection
- Testing
### 5. Hallucination reduction
- Techniques: citation enforcement, retrieval verification, fine-tuning, constrained decoding, self-consistency checking
- Evaluation using baseline queries
- Evaluate baseline queries towards vanilla LLM
### 6. Writing
- Explain domain-specific context
- Describe domain-specific challenges
- Definition of hallucination (rules misinterpretation, tonal drift, what else?)
- How to measure hallucination / accuracy of response?
- Try and explained techniques used in #5


## The research question

"To what extent does retrieval-augmented generation reduce factual hallucinations in TTRPG rule-lookup tasks, and how do retrieval parameters (chunk size, top-k) affect this reduction?"

## Requirements

- Python 3.11+
- [Poetry](https://python-poetry.org/docs/#installation)

## Setup

```bash
# Clone the repository
git clone <repo-url>
cd thesis-rag-morkborg

# Install dependencies
poetry install

# Activate virtual environment
poetry shell
```

## Project Structure

| Folder | Description |
|--------|-------------|
| `src/extraction/` | Processed data |
| `src/chunking/` | Text splitting strategies |
| `src/retrieval/` | Vector store, search |
| `src/generation/` | LLM calls, prompts |
| `src/evaluation/` | Metrics, annotation tools |
| `notebooks/` | Exploration, experiments |
| `data/raw/` | Source PDFs (not in repo) |
| `data/processed/` | Extracted text, chunks |
| `evaluation/` | Testing queries |

## Requirements

- Python 3.11+
- Poetry


## Setup

```
# Clone the repo
git clone https://github.com/nkhralovich/ttrpg-rag-assistant.git
cd ttrpg-rag-assistant

# Install deps
poetry install

# Install shell plugin
poetry self add poetry-plugin-shell

# Activate venv
poetry shell
```

## Data

Place source PDFs in `data/raw/`.

## Running
