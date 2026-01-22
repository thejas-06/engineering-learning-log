# Chinchilla Scaling Law: Why Data Matters as Much as Model Size

This note explains the Chinchilla Scaling Law and how it changed
the way large language models are designed and trained.

---

## Two basic building blocks
Before the law, remember this:

- **Parameters** → what the model *can* learn (capacity)
- **Tokens** → what the model *learns from* (experience)

Both must scale together.

---

## The old belief: bigger is always better
For years, the industry focused on:
- Increasing parameter count
- Training on relatively limited data

Example:
- Very large models trained on insufficient tokens

Analogy:
- A massive library with half the shelves empty

The model looks powerful but is under-trained.

---

## What the Chinchilla Scaling Law says
The **Chinchilla Scaling Law** states:

> The number of training tokens should be roughly **20× the number of model parameters**.

Examples:
- 3B parameters → ~60B tokens
- 70B parameters → ~1.4T tokens

---

## The Chinchilla experiment
Researchers at **Deepmind**
tested this idea using the **Chinchilla** model.

Key facts:
- Only 70B parameters
- Trained on ~1.4 trillion tokens
- Outperformed much larger models trained on less data

This proved that **data-starved giant models waste capacity**.

---

## Why this works (intuition)
Think of training athletes:
- Trainers = parameters
- Students = tokens

If you hire many trainers but give them too few students:
- Most trainers sit idle

If each trainer gets enough students:
- Learning becomes efficient
- Performance improves

Models behave the same way.

---

## What changed after Chinchilla
After this discovery:
- Model sizes became more conservative
- Training datasets grew massively
- Efficiency became more important than raw size

This directly influenced:
- Modern LLM training strategies
- Cost-aware model design
- Better performance-per-parameter

---

## Key insight
A model can be:
- Too small → underpowered
- Too large → under-trained

Optimal performance comes from **balanced scaling**.

---

## One-line takeaway
A well-fed smaller model can outperform a starving giant —
data and parameters must grow together.
