# Final Project – CSCI 420: Large Language Models

# Jinyan Kuang

## Overview

This repository contains the materials for my final project in CSCI 420, which explores fine-tuning GPT-2 on mental health counseling data to evaluate its ability to generate empathetic, context-appropriate responses.

The primary write-up is in `Final Report-CSCI420 LLM.pdf`, which addresses Exercises 1.1 through 1.6 (excluding Exercises 1.2, as indicated in the course email).

---

## All Content in Repository

### `Final Report-CSCI420 LLM.pdf`
- Full written report answering Exercises 1.1 to 1.6
- Exercise 1.1 is a sperate question
- Exercise 1.3-1.6: describe the task motivation, model structure, dataset, fine-tuning process, evaluation methods, and results

### `gpt2FineTune.ipynb`
- Contains code for training and evaluating GPT-2
- Includes:
  - Mental health conversation dataset (from HuggingFace)
  - Baseline GPT-2 model evaluation
  - Fine-tuned GPT-2 training on the dataset
  - Comparison between baseline and fine-tuned model outputs

### `utils.py` and `encoder.py`
- Helper files sourced from the `gpt2pico` GitHub repository
- Used for tokenization, encoding, and internal model operations during text generation
- These were part of our class practice on implementing a simplified GPT-2 model

---

## Summary of Work

1. **Baseline Evaluation**:  
   Used pretrained GPT-2 (`gpt2` from HuggingFace) to generate responses to mental health prompts. Evaluated outputs qualitatively and quantitatively (via log-likelihood).

2. **Fine-Tuning**:  
   Fine-tuned GPT-2 on a dataset of real-world counseling Q&A exchanges. Training was done using the HuggingFace `Trainer` API and causal language modeling objective.

3. **Comparison**:  
   Compared baseline and fine-tuned models using both:
   - Generated responses to real prompts
   - Negative log-likelihood scores to assess how well each model fits the reference responses

4. **Conclusion**:  
   Demonstrated that the fine-tuned model showed significantly better alignment with counseling tone, structure, and emotional sensitivity, highlighting the potential of LLMs for domain-specific support tasks.

