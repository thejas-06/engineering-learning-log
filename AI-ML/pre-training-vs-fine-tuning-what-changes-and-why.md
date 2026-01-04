# Pre-training vs Fine-tuning — What Changes and Why

This note explains the difference between pre-training and fine-tuning
and how companies actually build domain-specific AI systems.

---

## Pre-training
Pre-training is where a large language model learns general intelligence.

What happens:
- Model is trained on massive datasets (text, code, web data)
- Uses self-supervised learning (predicting the next token)
- Learns language, facts, reasoning patterns, and structure

Result:
- A general-purpose model like **ChatGPT**
- Broad knowledge, no company-specific rules

Mental model:
- College education for AI

---

## The limitation of pre-trained models
Even very strong models:
- Don’t know internal company policies
- Don’t understand private documents
- Don’t follow domain-specific constraints by default

For example:
- A finance assistant without financial rules is risky

---

## Fine-tuning
Fine-tuning adapts a pre-trained model to a specific domain or behavior.

What happens:
- Start with a pre-trained model
- Train further on curated examples
- Use domain data, feedback, and task-specific outputs

Result:
- More accurate
- More consistent
- Aligned with business needs

Mental model:
- On-the-job training after college

---

## Practical example (finance bot)
Instead of building a model from scratch:
- Use a pre-trained GPT model
- Fine-tune it with:
  - Portfolio examples
  - Company policies
  - Client interaction patterns

The model keeps its general intelligence
but behaves like a finance expert.

---

## Under the hood difference
Pre-training:
- Massive compute
- Billions of parameters
- Broad pattern learning

Fine-tuning:
- Smaller datasets
- Lower cost
- Targeted behavior shaping

---

## How companies actually use this
Most companies:
- Do NOT train models from scratch
- Use pre-trained models via APIs
- Add fine-tuning or wrappers for customization

These are often called “wrapper chatbots.”

---

## One-line takeaway
Pre-training creates intelligence; fine-tuning specializes it for real-world use.
