# Comparison of Pragmatic Competence of LLM For English and Bengali
 
**Master's Thesis — Linguistic Data Science**  
Ruhr University Bochum, 2026  
Author: Md Tasnimul Hasan Tashin  
Supervisor: Prof. Dr. Ralf Klabunde
 
---
 
## Overview
 
This repository contains all code and datasets used in the thesis. The study evaluates the pragmatic competence of ChatGPT (GPT-5.4 mini) in English and Bengali across three phenomena: scalar implicature, presupposition, and irony/sarcasm. A zero-shot binary multiple-choice question (MCQ) format was used across 600 test items — 300 per language.

## Datasets
 
### Scalar Implicature
- **Items per language:** 75 (25 per condition)
- **Conditions:** No Context (NC), Upper-bound QUD (UB), Lower-bound QUD (LB)
- **Scalar terms tested:** some (Bengali: কিছু) and or (Bengali: অথবা)
- **Source:** IMPPRES benchmark (Jeretic et al., 2020)
### Presupposition
- **Items per language:** 100 (50 per trigger type)
- **Conditions:** Affirmative (AFF), Negated (NEG)
- **Trigger types:** Change-of-state verbs (COS), Possessed definite descriptions (PDE)
- **Source:** IMPPRES benchmark (Jeretic et al., 2020)
### Irony and Sarcasm
- **Items per language:** 50 (25 sarcastic, 25 sincere)
- **Format:** Binary classification — sarcastic vs sincere
- **Source:** nikesh66/Sarcasm-dataset (GitHub)

### Results datasets (all phenomena)
All result files contain the same columns as the corresponding dataset file, plus:
 
| Column | Description |
|--------|-------------|
| MODEL_RESPONSE | The model's response (A or B) |
| CORRECT | Whether the response matched the expected answer (True/False) |

## Testing Notebook
 
`Thesis.ipynb` is organised into three sections:
 
**Section 1 — Scalar Implicature**  
 
**Section 2 — Presupposition**  

**Section 3 — Irony and Sarcasm**  

### API Configuration
- Model: `gpt-5.4-mini`
- Temperature: `0` (deterministic)
- Max tokens: `20`
- Mode: Zero-shot (no system prompt, no examples)
- Delay between requests: 0.5 seconds
### To replicate
1. Install the OpenAI Python library: `pip install openai`
2. Add your OpenAI API key at the top of the notebook
3. Run each section


## References
 
- Cho, W., & Kim, N. (2024). Pragmatic competence of language models: QUD manipulation for scalar implicature. *ACL Student Research Workshop*.
- Jeretic, P., Warstadt, A., Bhooshan, S., & Williams, A. (2020). Are natural language inference models IMPPRESsive? *ACL 2020*.
- Qiu, L., Duan, N., & Cai, D. (2023). Is ChatGPT a good NLI-Solver? *NALOMA 2023*.
- Yue, X., Song, Y., Cheng, Y., & Hu, B. (2024). Can large language models understand Chinese humor? *CCL 2024*.
- nikesh66. (n.d.). Sarcasm-dataset. GitHub. https://github.com/nikesh66/Sarcasm-dataset
