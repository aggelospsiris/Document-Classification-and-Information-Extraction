
# Document Classification and PDF Information Extraction

This project contains code for document classification using BERT-based embeddings and information extraction from PDF files. It includes three primary notebooks:
- `docs_classification.ipynb`: For clustering documents and extracting keywords using fine-tuned BERT embeddings.
- `extract_information_from_pdf.ipynb`: For extracting titles, abstracts, keywords, and authors from PDF files.
- `fine_tune_bert_model.ipynb`: For fine-tuning a BERT model on a specific dataset.

## Prerequisites

Ensure you have Python 3.8+ installed. You'll also need to install the required libraries, which are listed in `requirements.txt`.

## Installation

1. **Clone the repository** (if applicable) and navigate to the project directory.

2. **Install the required libraries**:
   ```bash
   pip install -r requirements.txt
   ```

## Notebooks Overview

### 1. Document Classification (`docs_classification.ipynb`)

This notebook performs the following tasks:
- Loads and preprocesses text data.
- Generates document embeddings using a fine-tuned BERT model.
- Clusters documents using K-Means and visualizes the results using t-SNE.
- Extracts keywords from clusters using Latent Dirichlet Allocation (LDA).
- Matches each cluster to predefined categories.
- Builds the final JSON output.

### 2. PDF Information Extraction (`extract_information_from_pdf.ipynb`)

This notebook focuses on:
- Extracting titles, abstracts, keywords, and authors from PDF files.
- Cleaning and normalizing text, including handling diacritical marks.
- Saving extracted information into CSV and JSON formats.

### 3. Fine-tuning BERT (`fine_tune_bert_model.ipynb`)

This notebook covers:
- Loading datasets suitable for BERT training.
- Fine-tuning a BERT model with masked language modeling.
- Evaluating the fine-tuned model's performance.

## Running the Notebooks

1. Start a Jupyter Notebook server:
   ```bash
   jupyter notebook
   ```

2. Open the desired notebook (e.g., `docs_classification.ipynb`) and follow the instructions within the cells.

## Additional Notes

- Ensure you have the required PDF files for the extraction tasks in the appropriate directory.
- You may need GPU support for faster BERT model training; otherwise, the process might be slow on a CPU.

## License

This project is licensed under the MIT License.
