# Multi-Document Abstractive Summarization (CNN/DailyMail)

This project benchmarks summarization model on the CNN/DailyMail dataset using ROUGE metrics.

## Models Implemented
- BART (facebook/bart-large-cnn)

## Dataset
- CNN/DailyMail v3.0.0 from Hugging Face datasets

## BART Results (10K samples)
Metric : Score 
rouge1: 0.3469
rouge2: 0.1347
rougeL: 0.2473
rougeLsum: 0.3214

Training time: ~30 minutes
Hardware used: Google Colab with Tesla T4 GPU

## Common Issues Encountered
- Issue - _cffi_backend error on local
  fix - Use Google Colab or uninstall soundfile

- Issue - fsspec ValueError: '**'
  fix - Downgrade fsspec to version 2023.6.0

- Issue - Low ROUGE scores
  fix - Increase training data size and epochs; tune learning rate, batch size, and decoding strategies


## How to Run

1. Clone the repository
2. Run the code
```bash
pip install -r requirements.txt

