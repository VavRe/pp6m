# Political User Profiling Research Repository [Double-Blind]

This repository contains the implementation code for our research paper submitted to ECIR 2025. For double-blind review purposes, the paper title and authors are not disclosed at this time.

> **Note**: This is a work in progress. The code is being cleaned and organized for better accessibility and reproducibility.

## Project Overview

This research presents novel approaches to political user profiling using large-scale tweet analysis, knowledge base creation, and advanced language models. The project encompasses multiple components from data preprocessing to stance evaluation.

## Main Components

### Data Processing
- Preprocessing pipeline for 7M+ tweets
- Unsupervised dataset curation for classifier training
- Domain-specific knowledge base creation
  - Seed node entities from Wikidata
  - Configurable timespan
  - Edge type specification
  - Wikipedia page collection

### Content Processing & Embedding
- Markdown-aware chunking system for 700+ Wikipedia articles
- Embedding generation using BGE-m3 model
- LanceDB integration for efficient storage and retrieval
- Cosine similarity calculations between Wikipedia pages and tweets

### Classification & Training
- 15K sample dataset curation for political content filtering
  - Binary classification (1: political, 0: non-political)
  - Threshold-based filtering using similarity metrics
- Tooka-BERT classifier fine-tuning
  - Frozen architecture with last 4 layers fine-tuned
  - 94% accuracy achieved on test set

### Domain Definition & Tweet Selection
- 800 domain-defining statements generated using GPT-4o mini
  - Reduced to 15 final statements
  - Based on user history analysis
- Three tweet selection methods implemented:
  1. Stratified sampling from K-means clusters
  2. Iterative elimination based on mean embedding similarity
  3. Mean embedding proximity selection

### User Profiling Methods
1. BM25-based approach
2. RAG@2 implementation
3. Amazon Approach (GPT4o-mini and Gemini Flash 1.5 for summarization)
4. Two novel proposed approaches (details in paper)

### Evaluation
- Stance prediction using GPT-4o mini and Gemini Flash 1.5
- Comprehensive evaluation metrics implementation
- Comparison between LLM predictions and human-annotated ground truth

## Repository Structure
```
📦 root
 ┣ 📂 preprocessing
 ┣ 📂 knowledge_base
 ┣ 📂 embeddings
 ┣ 📂 classification
 ┣ 📂 profiling
 ┣ 📂 evaluation
 ┣ 📂 utils
 ┗ 📂 configs
```

## Setup and Installation
[Coming Soon]

## Usage
[Coming Soon]

## Citation
Please note that citation information will be provided after the double-blind review process.

## License
[Coming Soon]

## Contact
For any questions regarding this repository, please open an issue in the repository's issue tracker.

## Acknowledgments
We thank the reviewers for their valuable feedback. Detailed acknowledgments will be added post-review.