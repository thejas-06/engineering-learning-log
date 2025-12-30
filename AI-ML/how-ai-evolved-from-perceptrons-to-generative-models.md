# How AI Evolved: From Perceptrons to Generative Models

This note captures the high-level evolution of AI systems over ~70 years,
focusing on *what changed at each stage* and *why it mattered*.

---

## 1957 — Perceptron
The first attempt at a “learning machine,” proposed by **Frank Rosenblatt**.

What it could do:
- Binary decisions (yes / no)
- Linear separation only

Mental model:
- One artificial neuron
- Draws a straight line to decide

Limitation:
- Too simple to model real-world complexity

---

## 1980s — Neural Networks + Backpropagation
Researchers realized one neuron wasn’t enough.

What changed:
- Many neurons connected together
- Errors propagated backward so all neurons learn together

This learning process became known as **backpropagation**.

Impact:
- Handwriting recognition
- Basic image and pattern recognition

Mental model:
- Group decision-making instead of a single opinion

---

## 2000s — Deep Learning
Neural networks became *deep*.

What changed:
- Multiple layers stacked together
- Each layer learned increasingly complex features

Analogy to remember:
- Balance → steering → acceleration when learning to ride a bike

Impact:
- Major improvements in vision, speech, and recognition tasks

---

## 2017 — Transformers
A major architectural shift introduced by the paper
**Attention is All You Need**.

What changed:
- Models stopped processing data strictly left-to-right
- Attention allowed any part of the input to relate to any other part

Mental model:
- Reading an entire book and instantly linking any two words

Impact:
- Massive improvement in language understanding
- Scaled extremely well with data and compute

---

## Present — Generative AI
Modern models don’t just understand data — they generate new data.

Examples:
- Large Language Models (text)
- Diffusion models (images)
- Multimodal models (text, image, audio, video)

Key insight:
- Creativity was not explicitly programmed
- Emerged from scale, data, and architecture

---

## One-line takeaway
Generative AI is not magic — it is the result of decades of layered improvements
in representation, learning, and architecture.
