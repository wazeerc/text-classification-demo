# Text Classification Demo

This project demonstrates text classification using Hugging Face Transformers in a Jupyter Notebook. It uses a pre-trained [DistilBERT model](https://huggingface.co/distilbert/distilbert-base-uncased-finetuned-sst-2-english) to classify user feedback from a Netflix dataset - positive or negative sentiment.

## Requirements
- Python 3.8+
- Jupyter Notebook
- [uv](https://github.com/astral-sh/uv) (for fast dependency management)
- [transformers](https://huggingface.co/docs/transformers/index) library
- [pandas](https://pandas.pydata.org/) for data manipulation
- [torch](https://pytorch.org/) for model inference

## Setup

1. Create a Python virtual environment (recommended):
  ```sh
    uv venv .venv
  ```

2. Activate the virtual environment:
- On Windows (PowerShell):
  ```sh
    .venv\Scripts\Activate.ps1
  ```
- On macOS/Linux:
  ```sh
    source .venv/bin/activate
  ```

3. Install dependencies in the activated environment using [uv](https://github.com/astral-sh/uv) (or pip):
  ```sh
    uv pip install transformers transformers[torch] pandas
  ```

4. Start Jupyter and open `notebook.ipynb`

## Usage
Run the notebook cells in order:
1. Load data from `./data/netflix.csv`
2. Classify feedback using the pipeline
3. View results in a table

## Data
The current dataset is a sample of [Netflix user feedback](https://www.kaggle.com/datasets/vishweshsalodkar/customer-feedback-dataset) stored in `./data/netflix.csv`.
You can replace this with your own dataset as long as it follows the same structure.

> [!TIP]
> Replace the `MODEL` and `DATASET` variables in the 1st cell of `notebook.ipynb` with any model and dataset you want to use.