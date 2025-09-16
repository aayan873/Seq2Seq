# Sequence Models: RNN & LSTM

This folder contains minimal PyTorch implementations of two fundamental sequence models:

1. **RNN for Q&A** - trained on a small custom Q&A dataset.
2. **LSTM for Text Generation** - trained on Shakespeare text to generate poetry.

---

## Files
- `100_Unique_QA_Dataset.csv` - custom Q&A dataset.
- `qna-using-rnn-pytorch.ipynb` - RNN-based Q&A model.
- `poetry-generation-lstm.ipynb` - LSTM-based text/poetry generation.
- `shakespeare.txt` - dataset for LSTM training.

---

## Key Ideas
- RNN captures short-term dependencies but struggles with long-range context.
- LSTM improves by using **gates** (forget, input, output), allowing better long-term memory.

---

## Results
- **Q&A model**: Learns to map short English questions → answers from the dataset.  
- **LSTM poetry**: Generates new text in Shakespearean style after training.

---

## Why this matters
RNNs and LSTMs are the **building blocks** for more advanced sequence models like **Seq2Seq** and **Transformers**.

