# SMM4H-HeaRD 2026 — Task 1: ADE Detection

System submission for [SMM4H-HeaRD 2026](https://healthlanguageprocessing.org/smm4h-2026/) Task 1 — Binary classification of multilingual social media posts for Adverse Drug Event (ADE) detection.

---

## Task

Given a social media post in one of 6 languages (English, German, French, Russian, Mandarin, Japanese), predict whether it mentions an Adverse Drug Event.

- **Type:** Binary Classification (`0` = no ADE, `1` = ADE mentioned)
- **Metric:** Unweighted Macro F1 across all languages

---

## Approach

- **Model:** XLM-RoBERTa Large (`xlm-roberta-large`)
- **Class imbalance:** Weighted cross-entropy loss
- **Extra data:** CADEC v2 translated data (German/French)
- **Threshold tuning:** Optimal threshold searched on dev set

## Results

| Model | Dev Macro F1 |
|-------|-------------|
| XLM-RoBERTa Base | 0.810 |
| XLM-RoBERTa Large | 0.841 |

---

## Setup

```bash
pip install transformers datasets scikit-learn torch accelerate pandas
```

---

## Team

| Name | Affiliation |
|------|-------------|
| [Mohammed Omar Faiaz] | [CUET] |
| [Abir Dey] | [CUET] |

---

## Competition Links

- [Task Page](https://healthlanguageprocessing.org/smm4h-2026/)
- [CodaBench](https://www.codabench.org/competitions/14124)
- [Google Group](https://groups.google.com/g/smm4h-heard-2026-task-1)
