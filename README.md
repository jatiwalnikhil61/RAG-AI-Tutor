# AI English Tutor

This repository contains two implementations of an AI-powered English tutoring system designed to generate engaging lessons based on various topics. The primary goal is to demonstrate different approaches to retrieving information, tokenizing text, and generating lessons using AI models.

## Repository Overview

The repository provides two distinct approaches for building an AI-based English tutor:

1. **AI_Tutor.ipynb** – A straightforward implementation that generates English lessons without the use of a vector database or advanced tokenization techniques. This notebook uses basic methods for text processing and retrieval to create lessons based on predefined content.
   
2. **AI_Tutor_VDB.ipynb** – An enhanced version that integrates a vector database (ChromaDB) for efficient retrieval of relevant content and uses NLTK for advanced sentence tokenization. This version demonstrates how to handle large corpora and generate lessons by extracting content using advanced retrieval mechanisms.

### Key Differences

- **Vector Database**: The `AI_Tutor_VDB.ipynb` implementation utilizes ChromaDB for storing and retrieving content. This allows for efficient querying and retrieval of relevant content for lesson generation.
  
- **Text Tokenization**: `AI_Tutor_VDB.ipynb` employs NLTK’s `sent_tokenize` function for sophisticated sentence splitting and chunking, ensuring that the retrieved content is processed and broken down properly. In contrast, `AI_Tutor.ipynb` uses simpler methods for handling text processing.
  
- **AI Lesson Generation**: Both implementations use an AI model for generating lessons, but the retrieval mechanism and content processing pipeline differ significantly, with the VDB version showcasing more robust retrieval through vector databases and tokenization.

## Files

- **`AI_Tutor.ipynb`**: A simpler version of the AI tutor without a vector database or NLTK-based text processing.
- **`AI_Tutor_VDB.ipynb`**: A more advanced version that utilizes a vector database and NLTK for efficient content retrieval and processing.

## Setup and Requirements

To run these notebooks, you will need to install the following dependencies, along with other dependencies used in the code:

```bash
pip install chromadb
pip install sentence-transformers
pip install nltk
pip install fpdf
pip install torch
```

Additionally, for `AI_Tutor_VDB.ipynb`, ensure you download the necessary NLTK tokenizers:

```bash
import nltk
nltk.download('punkt_tab')
```

## Usage

### Running the Simple AI Tutor (`AI_Tutor.ipynb`)

This notebook provides a basic implementation of lesson generation without relying on external databases for retrieval. Simply run the notebook cells and input the desired topic for lesson creation.

### Running the Vector Database AI Tutor (`AI_Tutor_VDB.ipynb`)

This version makes use of a vector database to retrieve relevant information efficiently. Follow these steps:

1. Add content to the vector database using the `add_content_to_vector_db` function or upload content from PDF files.
2. Generate a lesson by specifying a topic, and the model will retrieve relevant content and create an engaging lesson.
