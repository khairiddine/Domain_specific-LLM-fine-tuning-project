# 🏥 ChatDoctor: Medical AI Assistant
![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Unsloth](https://img.shields.io/badge/Optimization-Unsloth-green)
![Status](https://img.shields.io/badge/Status-Fine--Tuned-success)

A specialized Medical LLM fine-tuned on **100,000 patient-doctor conversations** using **Phi-3.5-mini** (4B).




## 📊 Project Details
*   **Model:** Microsoft Phi-3.5-mini-instruct (4B)
*   **Dataset:** [ChatDoctor-HealthCareMagic-100k](https://huggingface.co/datasets/lavita/ChatDoctor-HealthCareMagic-100k)
*   **Method:** LoRA Fine-tuning via Unsloth
*   **Training Time:** ~1.5 Hours on Tesla T4
*   **Validation Loss:** 1.47 (No overfitting)

## 💻 Local Usage
To run the model locally using Python:

```python
from unsloth import FastLanguageModel

# Load model + adapter directly
model, tokenizer = FastLanguageModel.from_pretrained(
    model_name = "khairi123/medical-phi35-chatdoctor",
    load_in_4bit = True,
)
FastLanguageModel.for_inference(model)

# ... (Add generation code here)