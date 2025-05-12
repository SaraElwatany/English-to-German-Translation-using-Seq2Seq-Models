# English-to-German Translation using Seq2Seq (LSTM)

This project implements a sequence-to-sequence (Seq2Seq) model with LSTM-based encoder and decoder to perform machine translation from English to German.

## Project Overview

The task is to translate English sentences into German using a basic Seq2Seq model architecture. It includes:

- **Data preprocessing and tokenization**
- **Embedding layers for input representation**
- **LSTM encoder and decoder with optional teacher forcing**
- **Training and evaluation pipelines**


## Model Architecture

### 🔤 Encoder
The encoder takes the source (English) sentence, embeds each token, and feeds it into a multi-layer LSTM. It returns the hidden and cell states that summarize the sentence.

### 💬 Decoder
The decoder receives the encoder's final hidden and cell states and predicts the target (German) sentence token by token. Teacher forcing can be used during training.

### 🔄 Seq2Seq Wrapper
A `Seq2Seq` class coordinates the encoder and decoder during training and inference, managing the passing of hidden states and input tokens.


## Requirements
- Python 3.7+
- PyTorch
- tqdm
- Hugging Face datasets
