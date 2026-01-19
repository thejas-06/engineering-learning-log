# Top Generative AI Terms – Part 2 (Interview Critical)

This note covers the next set of Generative AI terms that interviewers
commonly test once basics are clear.

---

## 1. GANs (Generative Adversarial Networks)
GANs consist of **two competing models**:

- Generator → creates fake data
- Discriminator → judges real vs fake

They train together until the generator becomes highly realistic.

Example:
- Generating photorealistic human faces that don’t exist

---

## 2. RLHF (Reinforcement Learning with Human Feedback)
RLHF is a training technique where:
- Humans rank or score AI outputs
- The model learns to prefer better responses

Why it matters:
- Improves safety
- Aligns outputs with human values
- Reduces harmful or useless responses

Example:
- **ChatGPT** became more helpful and safer using RLHF.

---

## 3. Fine-tuning
Fine-tuning adapts a **pre-trained model** to a specific domain or task.

How it works:
- Start with a general model
- Train further on smaller, specialized datasets

Example:
- Turning a general LLM into a medical assistant using clinical texts

Mental model:
- General education → specialization

---

## 4. Zero-shot Learning
Zero-shot learning means:
- Performing a task **without seeing examples**
- Relying purely on instruction understanding

Why it works:
- Large models learn broad patterns during pre-training

Example:
- Translating English to French without providing examples in the prompt

---

## 5. Few-shot Learning
Few-shot learning improves performance by:
- Showing a small number of examples in the prompt
- Letting the model infer the pattern

Example:
- Providing 3 labeled customer reviews before sentiment analysis

Key benefit:
- Custom behavior without retraining

---

## 7. Temperature
Temperature controls **randomness and creativity** in outputs.

How it behaves:
- Low temperature (e.g., 0.2) → deterministic, factual
- High temperature (e.g., 0.9) → diverse, creative

Important:
- This is a backend sampling parameter
- Not intelligence, but variability control

---

## One-line takeaway
These concepts explain **how models are trained, adapted, and controlled** —
the difference between using AI and understanding it.
