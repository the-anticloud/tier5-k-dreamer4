# 3-Seed Simulation — K_DREAMER4

**Seeds:** `87233` · `18570` · `52769`

**Seed method:** `sha256("K_DREAMER4")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_DREAMER4`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.9677 | 0.1249 | ±0.2448 |
| throughput_tokens_per_sec | 395.6 | 27.267 | ±53.4433 |
| p50_latency_ms | 45.6767 | 3.7207 | ±7.2926 |
| p99_latency_ms | 120.3 | 7.8871 | ±15.4587 |
| ttft_ms | 26.33 | 1.7439 | ±3.418 |
| mmlu_proxy | 0.757 | 0.0261 | ±0.0512 |
| hellaswag_proxy | 0.774 | 0.038 | ±0.0745 |
| truthfulqa_proxy | 0.6019 | 0.0375 | ±0.0735 |
| arc_proxy | 0.6814 | 0.0352 | ±0.069 |
| complexity_cyclomatic | 4.58 | 0.3269 | ±0.6407 |
| maintainability_index | 75.48 | 4.3347 | ±8.496 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 80.4 | 2.9631 | ±5.8077 |
| test_coverage_pct | 54.2333 | 10.585 | ±20.7466 |
| doc_coverage_pct | 66.7667 | 8.695 | ±17.0422 |
| memory_mb | 50.5 | 0.7071 | ±1.3859 |
| gpu_util_pct | 67.9667 | 3.2294 | ±6.3296 |
| openssf_score | 7.0533 | 0.2963 | ±0.5807 |
| eu_ai_act_compliance_pct | 83.2333 | 6.144 | ±12.0422 |
| slsa_level | 1.6667 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 87233 | Seed 18570 | Seed 52769 |
|--------|------------|------------|------------|
| trl_score | 6.792 | 7.071 | 7.04 |
| throughput_tokens_per_sec | 403.7 | 424.2 | 358.9 |
| p50_latency_ms | 49.99 | 46.13 | 40.91 |
| p99_latency_ms | 109.3 | 127.4 | 124.2 |
| ttft_ms | 24.58 | 28.71 | 25.7 |
| mmlu_proxy | 0.72 | 0.7754 | 0.7755 |
| hellaswag_proxy | 0.7352 | 0.8256 | 0.7613 |
| truthfulqa_proxy | 0.5519 | 0.6114 | 0.6423 |
| arc_proxy | 0.6808 | 0.7248 | 0.6385 |
| complexity_cyclomatic | 5.04 | 4.31 | 4.39 |
| maintainability_index | 78.51 | 69.35 | 78.58 |
| security_issues_high | 0 | 0 | 1 |
| dependency_freshness_pct | 77.6 | 84.5 | 79.1 |
| test_coverage_pct | 69.2 | 46.5 | 47.0 |
| doc_coverage_pct | 54.8 | 75.2 | 70.3 |
| memory_mb | 50 | 50 | 51.5 |
| gpu_util_pct | 64.8 | 66.7 | 72.4 |
| openssf_score | 7.0 | 6.72 | 7.44 |
| eu_ai_act_compliance_pct | 86.7 | 74.6 | 88.4 |
| slsa_level | 1 | 2 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._