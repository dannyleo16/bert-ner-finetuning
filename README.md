# BERT NER Fine-Tuning

This project implements fine-tuning of a BERT model for Named Entity Recognition (NER) using Spanish emergency call transcripts.

---

## Task

Named Entity Recognition (NER)

Entities detected:

PER → Person  
LOC → Location

---

## Model

Base model:

bert-base-spanish-wwm-cased

Framework:

Hugging Face Transformers

---

## Dataset

Emergency call transcripts from ECU-911 system.

Due to privacy restrictions the dataset is not publicly available.

---

## Results

Accuracy: 0.95  
Precision: 0.79  
Recall: 0.85  
F1-score: 0.81

---

## Hugging Face Model

https://huggingface.co/dannyLeo16/ner_model_bert_base

---

## Example Usage

```python
from transformers import pipeline

ner = pipeline(
    "ner",
    model="dannyLeo16/ner_model_bert_base",
    tokenizer="dannyLeo16/ner_model_bert_base"
)

text = "Hay una persona herida en la avenida Loja"

result = ner(text)

print(result)
