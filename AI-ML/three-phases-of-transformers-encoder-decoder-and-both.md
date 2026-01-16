# The Three Phases of Transformers: Encoder, Encoder–Decoder, Decoder

This note explains the three major transformer architectures and
what each one is optimized to do.

---

## Why this distinction matters
All transformers share the same core ideas:
- Self-attention
- Feedforward networks
- Positional information

But how **encoders and decoders are arranged** changes what the model
is best at: understanding, generating, or transforming text.

---

## 1. Encoder-Only Models (The Readers)
Example: **BERT**

How they work:
- Input text goes through encoder layers
- The model builds rich contextual representations
- No text generation happens

What they are best at:
- Text classification
- Sentiment analysis
- Embeddings
- Information retrieval
- Question answering (extractive)

Mental model:
- Read deeply, don’t speak

Key strength:
- Understanding meaning and relationships in text

---

## 2. Encoder–Decoder Models (The Translators)
Examples:
- **Flan-T5**
- **BART**
- **Marian**

How they work:
- Encoder understands the input
- Decoder generates output step by step
- Cross-attention aligns input meaning with output generation

What they are best at:
- Machine translation
- Summarization
- Text-to-text tasks
- Paraphrasing

Mental model:
- Read → then rewrite

Key strength:
- Transforming one piece of text into another

---

## 3. Decoder-Only Models (The Storytellers)
Examples:
- **GPT Family of models**
- **Llama**
- **Claude**

How they work:
- Input is fed directly into the decoder
- Model predicts the next token autoregressively
- Continues until a response is complete

What they are best at:
- Chatbots
- Creative writing
- Code generation
- Open-ended reasoning

Mental model:
- Speak based on everything seen so far

Key strength:
- Flexible generation and conversation

---

## How to remember the split
- Encoder-only → **understand**
- Encoder–decoder → **transform**
- Decoder-only → **generate**

Same transformer idea, different optimization goals.

---

## Why all three still matter
No single architecture is “better” than the others.

Each exists because:
- Different problems need different inductive biases

Modern AI systems often combine them.

---

## One-line takeaway
Transformers aren’t one model — they’re a family, and the encoder/decoder
choice decides what the model is good at.
