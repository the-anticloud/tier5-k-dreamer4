# Developer Cookbook — K_DREAMER4
**Stack:** Python 3.11, PyTorch 2.10+, DreamerV3 architecture, PAX 27B, AIOSS_FORMAT
**Domain:** DreamerV4: world model with PAX 27B for embodied agent imagination and planning

## World model rollout
```python
from k_dreamer4 import DreamerWorldModel

model = DreamerWorldModel(
    checkpoint="./dreamer4_checkpoint/",
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./dreamer4.aioss"
)

# Imagine 10 steps ahead
trajectory = model.imagine(
    current_obs=robot_camera_frame,
    action_sequence=["move_forward", "turn_left", "grasp"],
    horizon=10
)
print(f"Predicted reward: {trajectory.expected_reward:.3f}")
print(f"Collision probability: {trajectory.collision_prob:.2%}")
```

## Language-conditioned planning
```python
plan = model.plan_from_language(
    goal="Move to the charging station without hitting obstacles",
    pax_model="./pax-27b-q4.gguf"
)
print(f"Plan actions: {plan.action_sequence}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
