# Top 10 Generative AI Terms You Must Understand

This note captures the most important Generative AI terms that
interviewers expect you to understand conceptually — not just by name.

---

## 1. Generative AI
Generative AI refers to systems that **create new content** instead of
just analyzing or retrieving existing data.

What it can generate:
- Text
- Images
- Audio
- Code
- Video

---

## 2. Model
A model is a **mathematical structure** (usually a neural network)
trained on large datasets to learn patterns.

What it does:
- Takes input
- Applies learned patterns
- Produces output

Example:
- Completing sentences
- Generating code

Mental model:
- A trained brain.

---

## 3. Parameters
Parameters are the **adjustable weights** inside a model.

What they control:
- How strongly inputs influence outputs
- The probability of the next token

Important:
- Users never directly edit parameters
- They are learned during training

Large models can have **billions of parameters**.

---

## 4. Tokens
Tokens are the **smallest units** a model processes.

They can be:
- Words
- Sub-words
- Characters
- Punctuation

Example:
“Hello, world!”
→ [Hello] [,] [world] [!]

Everything in an LLM ultimately becomes tokens.

---

## 5. Embeddings
Embeddings are **numerical vector representations** of tokens,
images, or concepts.

Key property:
- Similar meanings → vectors close together

Example:
- “Apple” and “banana” are closer than “apple” and “car”

Embeddings enable:
- Semantic search
- Recommendations
- RAG systems

---

## 6. Transformer
A transformer is a neural network architecture introduced in
**2017 paper by google**.

What makes it special:
- Uses attention instead of recurrence
- Processes sequences in parallel
- Scales extremely well

---

## 7. Attention
Attention allows the model to **focus on important tokens**.

What it does:
- Assigns importance weights
- Connects related words, even if far apart

Example:
In “The cat sat on the mat”
attention links “cat” with “sat”.

Attention is how context is understood.

---

## 8. Diffusion Models
Diffusion models generate data by:
- Starting from noise
- Gradually removing noise step by step

Mental analogy:
- Turning static into a clear image

Example:
- **Stable diffusion**
creates images by iterative denoising.

---

## 9. Training
Training is the process of **adjusting parameters** so the model learns
patterns from data.

Typically involves:
- Large datasets
- Optimization algorithms
- Massive compute

Training is expensive and done once.

---

## 10. Inference
Inference is when the **trained model is used** to generate outputs.

What happens:
- No learning
- Only prediction

Example:
- Chatting with an AI
- Generating images
- Writing code

Inference is fast compared to training.

---

## Final mental model
- Training builds intelligence
- Inference uses intelligence
- Architecture defines capability
- Data defines quality

---

## One-line takeaway
If you truly understand these terms, you’re already past beginner-level
Generative AI.
