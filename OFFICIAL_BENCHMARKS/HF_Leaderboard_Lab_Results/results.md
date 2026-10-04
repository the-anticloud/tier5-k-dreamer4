# HF_Leaderboard_Lab_Results

**Project:** `K_DREAMER4`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `danijar/dreamerv3`  
**Commit:** `e3f02248693a`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **47.67 ms** |
| Min latency | 41.54 ms |
| Max latency | 55.79 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **33** |
| Tokenization latency | 0.99 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.587 |
| Classification latency | 117.48 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_DREAMER4 (danijar/dreamerv3) — 95 files, 10448 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'dreamer', '##4', '(', 'dani', '##jar', '/', 'dreamer', '##v', '##3', ')', '—', '95', 'files', ',', '104', '##48', 'source']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_