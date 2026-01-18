# Reducing Hallucinations in RPG Session Support Systems with RAG

## Plan

### 1. Corpus & Baseline
- Corpus assembly (core rulebook, what else?)
- Create and annotate baseline queries
- Definition of hallucination (rules misinterpretation, tonal drift, what else?)
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
### 6. Writing 💅

## The research question

"To what extent does retrieval-augmented generation reduce factual hallucinations in TTRPG rule-lookup tasks, and how do retrieval parameters (chunk size, top-k) affect this reduction?"

## Project structure

# Reducing Hallucinations in RPG Session Support Systems with RAG

Master's thesis project exploring retrieval-augmented generation for TTRPG (Mörk Borg) session support.

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
| `src/extraction/` | PDF processing |
| `src/chunking/` | Text splitting strategies |
| `src/retrieval/` | Vector store, search |
| `src/generation/` | LLM calls, prompts |
| `src/evaluation/` | Metrics, annotation tools |
| `notebooks/` | Exploration, experiments |
| `data/raw/` | Source PDFs (not in repo) |
| `data/processed/` | Extracted text, chunks |
| `evaluation/` | Query sets, annotations |
| `configs/` | Experiment parameters |
| `results/` | Experiment outputs |
| `tests/` | Unit tests |

## Requirements

- Python 3.11+
- Poetry


## Setup

```
# Clone the repository
git clone <repo-url>
cd ttrpg-rag-assistant

# Install dependencies
poetry install

# Activate virtual environment
poetry shell
```

## Data

Place source PDFs in `data/raw/`.

## Running

```
poetry run jupyter notebook
poetry run python src/script.py
```
