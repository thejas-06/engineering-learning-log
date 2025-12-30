# Six Core Types of Generative AI Models

This note captures the main families of generative models and
what each one is fundamentally good at.

---

## 1. GANs (Generative Adversarial Networks)
Two neural networks compete with each other.

How it works:
- Generator creates fake data from noise
- Discriminator tries to detect fakes
- Both improve through competition

Mental analogy:
- Forger vs detective

What they are good at:
- Realistic image generation
- Deepfakes
- Style imitation

---

## 2. VAEs (Variational Autoencoders)
Models that learn to compress and reconstruct data.

How it works:
- Encode data into a latent space
- Decode it back to original form

Mental analogy:
- Smart compression (zip + creativity)

What they are good at:
- Smooth interpolation
- Face blending
- Representation learning

---

## 3. Autoregressive Models
Models that generate data step by step.

How it works:
- Predict the next token based on previous ones
- Repeat this process until completion

Mental analogy:
- “Finish the sentence” game

What they are good at:
- Text generation
- Language modeling
- Chat systems

---

## 4. RNNs (Recurrent Neural Networks)
Sequential models with memory loops.

Problem:
- Forget long-range information (vanishing gradients)

Fix:
- LSTM and GRU introduce gates to control memory

Mental analogy:
- Forgetting page 1 while reading page 100

What they are good at:
- Time-series
- Sequential data (limited context)

---

## 5. Transformers
Models based on self-attention.

How it works:
- Every token can attend to every other token
- Uses positional encoding and multi-head attention

Mental analogy:
- Reading an entire book and instantly connecting clues across chapters

What they are good at:
- Long-context understanding
- Language, vision, multimodal tasks

This architecture powers modern LLMs.

---

## 6. Reinforcement Learning (RLHF)
Models learn from rewards instead of examples.

How it works:
- Humans rate model outputs
- Model learns preferences via reward signals

Mental analogy:
- Training behavior using feedback

What it is used for:
- Alignment
- Safety
- Improving response quality

---

## One-line takeaway
Different generative models exist because they solve different generation problems —
from realism, to memory, to alignment.
