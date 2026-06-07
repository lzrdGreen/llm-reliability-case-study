# LLM Reliability Case Study - Qwen2.5-0.5B-Instruct

This repository evaluates multi-stage hallucination detection and factual validation guardrails using the Qwen2.5-0.5B-Instruct model. The analysis focuses on the tension between internal generation confidence (consensus) and external factual truth.

---

## Case Study Link

* **[View Jupyter Notebook](https://github.com/lzrdGreen/llm-reliability-case-study/blob/main/llm_reliability_case_study.ipynb)**

---

## Evaluation Architecture

* **Stage 1 (Generation):** Samples multiple text streams across adversarial and abstract prompts.
* **Stage 2 (Statistical Sorting):** Tracks internal stability metrics, including Semantic Divergence Drift, Consensus Density, and Cross-Encoder Relevance to flag epistemic risk.
* **Stage 3 (Deterministic Truth Gate):** Evaluates candidate branches via an external Ground Truth Registry and a dual-channel Natural Language Inference (NLI) pipeline measuring completeness (Positive Pillars) and integrity (Forbidden Claims).

---

## Primary Dependencies

```text
torch
transformers
sentence-transformers
accelerate
spacy
en_core_web_sm
numpy
scipy
pydantic
