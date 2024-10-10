
# Document Classification and Information Extraction

This project focuses on extracting information and classifying documents using machine learning techniques, specifically through a combination of BERT-based models and graph-based methods. The task involves processing PDF files to extract titles and authors, and classifying the documents into predefined categories.

## Table of Contents
- [Project Overview](#project-overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The objective of this project is to develop a machine learning pipeline that:
1. Extracts titles and authors from PDF documents.
2. Classifies each document into one of the predefined categories using two approaches:
   - BERT-based approach with LDA (Latent Dirichlet Allocation)
   - Graph-based approach using Node2Vec and BM25

The predefined categories include:
- Tables
- Classification
- Key Information Extraction
- Optical Character Recognition
- Datasets
- Document Layout Understanding
- Others

## Requirements
This project uses Python and several external libraries. Below is a list of the main dependencies:
- `PyTorch` and `Transformers` for BERT-based operations.
- `PyMuPDF` for extracting text from PDF files.
- `Node2Vec` and `NetworkX` for graph-based embeddings.
- `scikit-learn` for clustering and evaluation.
- `matplotlib` and `seaborn` for visualization.
- `numpy` and `pandas` for data manipulation.

## Installation
To get started with this project, you'll need to install the required libraries. You can do this using the following commands:

```bash
# Clone the repository
git clone https://github.com/your-repository/document-classification

# Change directory to the project folder
cd document-classification

# Create a virtual environment (optional but recommended)
python3 -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`

# Install the required dependencies
pip install -r requirements.txt
```


## Usage

### Step 1: Information Extraction
Run the `extract_information_from_pdf.ipynb` notebook to extract titles and authors from the PDF files. This will use Named Entity Recognition (NER) to identify and extract relevant information.

### Step 2: Document Classification using BERT-LDA
Open and execute the `docs_classification.ipynb` notebook. This notebook will:
- Generate embeddings using a BERT model.
- Use LDA for topic detection to refine the categorization.
- Classify documents into the predefined categories.

### Step 3: Document Classification using Graph-Based Approach
Run the `gnn_classification.ipynb` notebook. This notebook performs the following tasks:
- Creates a graph representation of the documents using words and their BM25 importance.
- Uses Node2Vec to generate embeddings for graph nodes.
- Clusters documents and matches them to the most relevant categories based on similarity.

### Step 4: Output
The final categorized results are saved in the `categorized_documents.json` file. This file contains the extracted titles, authors, and the classification results.

## Methodology
- **BERT-based Model with LDA**: Combines semantic text embeddings with topic modeling to enhance document classification accuracy.
- **Graph-based Model with Node2Vec and BM25**: Builds a graph of document relationships using word importance to generate node embeddings for clustering.

## Results
The combination of these two approaches offers a comprehensive analysis of document content, with each method complementing the other for improved classification accuracy.

## Contributing
Contributions to this project are welcome! If you find any issues or have ideas for improvements, feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
