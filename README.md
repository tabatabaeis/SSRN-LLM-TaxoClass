# Can Large Language Models Serve as Effective Classifiers for Hierarchical Multi-Label Classification of Scientific Documents at Industrial Scale?

This repository contains the code and data for our paper "Can Large Language Models Serve as Effective Classifiers for Hierarchical Multi-Label Classification of Scientific Documents at Industrial Scale?", accepted at COLING2025-Industry Track.

## Authors
- Seyed Amin Tabatabaei (Elsevier)
- Sarah Fancher (SSRN)
- Michael Parsons (SSRN)
- Arian Askari (Leiden University)

## Overview
This project explores the use of Large Language Models (LLMs) for hierarchical multi-label classification of scientific documents at an industrial scale. We present novel methods that combine the strengths of LLMs with dense retrieval techniques to overcome challenges in classifying documents across thousands of dynamic labels.

## Repository Structure

### Notebooks
The notebooks should be run in the following order:

1. `01_json_to_dataframe.ipynb`: Initial data preprocessing
2. `02-hierarchical_approach_evaluate_labels.ipynb`: Hierarchical evaluation of labels
3. `03_rank_labels_biencoder.ipynb`: Ranking labels using bi-encoder
4. `04_rerank_labels_gpt.ipynb`: Re-ranking labels using GPT
5. `05_proposed_approach.ipynb`: Main proposed approach
6. `05a_ablation_no_parent.ipynb`: Ablation study without parent nodes
7. `06_reduce_labels_gpt.ipynb`: Label reduction using GPT
8. `06a_ablation_random_reduction.ipynb`: Ablation study with random reduction

### Support Files
- `utils.ipynb`: Utility functions
- `config.ipynb`: Configuration settings
- `.gitignore`: Git ignore rules

### Dataset
The `dataset` folder contains:
- `ABSTRACT_all.json`: Metadata for all 100 articles used in the study
- `separate_jsons/`: Individual JSON files for each article
- `model_outputs_and_SME_annotations/`: Model results and SME annotations for each article

## Environment Setup

### Databricks
The notebooks were created in a Databricks environment. Some commands (like `%run`) are Databricks-specific. Users may need to modify these commands based on their environment.

### Azure OpenAI Setup
The code uses Azure OpenAI services for LLM interactions. To use this code:

1. Set up your Azure OpenAI environment
2. Modify the API settings in `utils.ipynb` with your:
   - API key
   - Azure environment details
   
Alternatively, you can modify the code to work with other LLM providers (e.g., OpenAI directly).

## Contact
For questions or issues, please contact:
Seyed Amin Tabatabaei (s.tabatabaei@elsevier.com)