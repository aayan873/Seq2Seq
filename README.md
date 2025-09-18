# English → Hindi Translator (Seq2Seq with and without Attention)

I built a simple English → Hindi translator using sequence-to-sequence models in PyTorch.
The project explores two versions:
1. **Basic Encoder–Decoder model (Encoder–Decoder with LSTM)**
2. **Encoder–Decoder with Attention (Bahdanau-style additive attention)**

---

## Files
- `English-to-hindi-using-encoder-decoder.ipynb` - Encoder-Decoder without attention.
- `English-to-hindi-using-encoder-decoder_with_attention.ipynb` - Encoder-Decoder with attention.
- Training & evaluation scripts (BLEU score included).

---

## Key Ideas
- **Without Attention**: Decoder relies only on the final hidden state of the encoder → can lose information in long sentences.  
- **With Attention**: Decoder dynamically “looks back” at relevant encoder states → solves the problem of information lose, improves translation quality.

---

## Comparison (English → Hindi translation task)

| Model               | BLEU Score | Example Output Quality |
|----------------------|------------|-------------------------|
| Seq2Seq (no attention) | **0.13**    | Sentences often incomplete or repetitive |
| Seq2Seq + Attention   | **0.21**    | More fluent, better word alignment |

At first glance, scores like 0.13 and 0.21 look small.
That’s expected here because the dataset is fairly limited, the models are kept simple, and BLEU itself is harsh on languages like Hindi where word order can vary a lot.

What actually matters is the relative jump = going from 0.13 to 0.21 is almost a 60% improvement. 
**Attention improved performance and generated more natural translations.**

---

## Why this matters
- This project demonstrates **how attention makes a real difference** in sequence-to-sequence tasks.  
- It also builds intuition for how modern Transformers work (which are essentially attention-only models).
