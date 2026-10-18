# Byte Pair Encoding (BPE) Tokenizer Notebook

This project contains a Jupyter notebook, `byte_pair.ipynb`, that trains a byte-level BPE tokenizer on the WikiText-2 dataset and saves it in a Hugging Face-compatible format.

## Overview

The notebook walks through a complete tokenizer workflow:

- Loads the `Salesforce/wikitext` dataset
- Cleans and normalizes raw text lines
- Removes empty and duplicate entries
- Trains a `tokenizers` BPE model with special tokens such as `[PAD]`, `[UNK]`, `[CLS]`, `[SEP]`, and `[MASK]`
- Saves the trained tokenizer as `bpe_tokenizer.json`
- Evaluates tokenization quality using example metrics
- Exports the tokenizer for reuse with `transformers.AutoTokenizer`

## Files

- `byte_pair.ipynb` — main notebook with all code cells
- `bpe_tokenizer.json` — trained tokenizer saved in tokenizers JSON format
- `wikitext_bpe_tokenizer/` — Hugging Face-compatible saved model directory (created when the notebook is run)

## Dependencies

The notebook uses the following Python libraries:

- `datasets`
- `tokenizers`
- `transformers`
- `pandas`

Install them with:

```bash
pip install datasets tokenizers pandas transformers
```

## How to run

1. Open `byte_pair.ipynb` in Jupyter or VS Code Notebook mode.
2. Run the cells in order from top to bottom.
3. Wait for the dataset download and tokenizer training to finish.
4. Use the saved tokenizer for encoding and decoding new text.

## Example purpose

This notebook is useful for learning and experimenting with:

- byte-level tokenization
- subword models
- BPE training from scratch
- saving and reloading tokenizers for downstream NLP tasks

## Notes

- The dataset is downloaded from the Hugging Face Hub. Internet access and a valid Hugging Face connection may be required.
- Large dataset operations may take time depending on your machine and network speed.
- The notebook includes preprocessing and deduplication steps to keep the training corpus cleaner and more efficient.
