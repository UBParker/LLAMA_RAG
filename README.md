---

# LLaMA RAG Model with Meta's LLaMA Model

WORK IN PROGRESS - Only notebooks 1 and 2 have been tested

In the spirit of the AI revolution this repository was authored by Ashley Marie Parker, Ph.D. with assistance from ChatGPT 4.0 mini.

This repository provides an example of building a Retrieval-Augmented Generation (RAG) model using Meta's LLaMA model. The model is designed to ingest website data, process it, and enable efficient retrieval-based responses using state-of-the-art RAG techniques.

## Table of Contents
- [Overview](#overview)
- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
  - [1. Apply for Meta’s LLaMA Model Access](#1-apply-for-metas-llama-model-access)
  - [2. Install Required Python Packages](#2-install-required-python-packages)
  - [3. Download the LLaMA Model](#3-download-the-llama-model)
- [Project Structure](#project-structure)
- [Usage](#usage)

## Overview
This project demonstrates how to create a RAG model using Meta’s LLaMA language model. The model is retrained with information from a specified website, enabling it to answer questions based on that site’s content.

## Requirements
- **Python** 3.10 or higher
- **Hugging Face Transformers** library
- **Meta’s LLaMA model files** (see setup instructions below)

## Setup Instructions

### 1. Apply for Meta’s LLaMA Model Access
Meta’s LLaMA models require direct access approval:
1. Visit Meta’s [LLaMA model access page](https://www.llama.com/llama-downloads/) to apply.
2. Once approved, Meta will email you a signed download URL.

### 2. Install Required Python Packages
Install the necessary packages using `pip`:
```bash
pip install transformers torch faiss-cpu sentence-transformers beautifulsoup4 requests

```

### 3. Download the LLaMA Model

Once you have received the signed URL from Meta via email:
1. Ensure you have Meta’s `llama` CLI tool installed.
2. Use the `llama` command to download the model, specifying the URL when prompted.

#### Example Command:
```bash
llama model download --source meta --model-id Llama3.2-90B-Vision-Instruct
```

When prompted, paste the signed URL exactly as provided in the email.

## Project Structure
The repository includes:
- **Jupyter notebooks** for different stages of setting up the RAG model.
- **Data directories** to store retrieved embeddings, model checkpoints, etc.

## Usage

1. **Run the Jupyter Notebooks**:
   - Start with `01_Data_Preparation.ipynb` to scrape and preprocess content.
   - Use `02_Vector_Store_Creation_and_Retrieval.ipynb` to embed the content and create a vector store.
   
2. **Query the Model**:
   - Use `03_Query_Model.ipynb` to interact with the model, retrieving answers based on website data.

This project provides an end-to-end setup, from data ingestion to retrieval and generation, using Meta’s LLaMA model.




