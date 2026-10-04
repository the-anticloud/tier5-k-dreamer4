# Deploy Guide — K_DREAMER4
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, DreamerV3 architecture, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, T4 GPU for inference, A100 for training. Custom DreamerV4 implementation.

## Environment
T4 GPU for inference (world model rollouts). A100 for training. 32GB RAM.

## AIOSS Integration
```bash
aioss init --module K_DREAMER4 --output ./k_dreamer4.aioss
aioss append --chain ./k_dreamer4.aioss --payload ./output.bin --module K_DREAMER4
aioss verify --chain ./k_dreamer4.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_DREAMER4",
    aioss_chain="./K_DREAMER4.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_DREAMER4.aioss --verbose
python -m K_DREAMER4.tests.smoke
```
