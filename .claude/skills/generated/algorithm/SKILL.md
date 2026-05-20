---
name: algorithm
description: "Skill for the Algorithm area of ppq. 60 symbols across 15 files."
---

# Algorithm

60 symbols | 15 files | Cohesion: 75%

## When to Use

- Working with code in `ppq/`
- Understanding how PPQuantFunction_toInt, PPQLinearQuant_toInt, PPQuantFunction work
- Modifying algorithm-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/quantization/algorithm/training.py` | __init__, __init__, __call__, LSQDelegator, RoundTuningDelegator (+15) |
| `ppq/quantization/algorithm/equalization.py` | key_value_from_upstream, scale_to_upstream, scale_to_downstream, equalize, activation_equalize (+7) |
| `ppq/core/quant.py` | has_property, to_dict, exponent_bits, channel_axis |
| `ppq/quantization/optim/legacy.py` | __init__, initiate_rounding, __call__, AdaRoundDelegator |
| `ppq/quantization/qfunction/linear.py` | PPQLinearQuant_toInt, forward, forward |
| `ppq/quantization/algorithm/exprimental.py` | BanditDelegator, roll, __call__ |
| `ppq/quantization/qfunction/__init__.py` | PPQuantFunction_toInt, PPQuantFunction |
| `ppq/samples/custimize_quant_func.py` | __call__, MyQuantDelegator |
| `ppq/core/ffi.py` | LinearQuantize_T, LinearQuantize_C |
| `tests/test_cuda_kernel.py` | __TEST_QUANTIZE_LT__, __TEST_QUANTIZE_LC__ |

## Entry Points

Start here when exploring this area:

- **`PPQuantFunction_toInt`** (Function) — `ppq/quantization/qfunction/__init__.py:46`
- **`PPQLinearQuant_toInt`** (Function) — `ppq/quantization/qfunction/linear.py:217`
- **`PPQuantFunction`** (Function) — `ppq/quantization/qfunction/__init__.py:9`
- **`TorchQuantizeDelegator`** (Class) — `ppq/executor/torch.py:42`
- **`BanditDelegator`** (Class) — `ppq/quantization/algorithm/exprimental.py:11`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `TorchQuantizeDelegator` | Class | `ppq/executor/torch.py` | 42 |
| `BanditDelegator` | Class | `ppq/quantization/algorithm/exprimental.py` | 11 |
| `LSQDelegator` | Class | `ppq/quantization/algorithm/training.py` | 317 |
| `RoundTuningDelegator` | Class | `ppq/quantization/algorithm/training.py` | 423 |
| `RoundTruningDelegator` | Class | `ppq/quantization/algorithm/training.py` | 528 |
| `AdaRoundDelegator` | Class | `ppq/quantization/optim/legacy.py` | 66 |
| `MyQuantDelegator` | Class | `ppq/samples/custimize_quant_func.py` | 11 |
| `PPQuantFunction_toInt` | Function | `ppq/quantization/qfunction/__init__.py` | 46 |
| `PPQLinearQuant_toInt` | Function | `ppq/quantization/qfunction/linear.py` | 217 |
| `PPQuantFunction` | Function | `ppq/quantization/qfunction/__init__.py` | 9 |
| `has_property` | Method | `ppq/core/quant.py` | 254 |
| `to_dict` | Method | `ppq/core/quant.py` | 297 |
| `exponent_bits` | Method | `ppq/core/quant.py` | 849 |
| `channel_axis` | Method | `ppq/core/quant.py` | 857 |
| `initiate_rounding` | Method | `ppq/quantization/optim/legacy.py` | 89 |
| `key_value_from_upstream` | Method | `ppq/quantization/algorithm/equalization.py` | 29 |
| `scale_to_upstream` | Method | `ppq/quantization/algorithm/equalization.py` | 138 |
| `scale_to_downstream` | Method | `ppq/quantization/algorithm/equalization.py` | 173 |
| `equalize` | Method | `ppq/quantization/algorithm/equalization.py` | 321 |
| `activation_equalize` | Method | `ppq/quantization/algorithm/equalization.py` | 394 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Calib_block → Is_activated` | cross_community | 5 |
| `Optimize → Push` | cross_community | 5 |
| `Optimize → Pop` | cross_community | 5 |
| `Optimize → Push` | cross_community | 5 |
| `Optimize → Pop` | cross_community | 5 |
| `Optimize → Empty` | cross_community | 5 |
| `Optimize → Push` | cross_community | 5 |
| `Optimize → Pop` | cross_community | 5 |
| `Optimize → Empty` | cross_community | 5 |
| `Optimize → Push` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| IR | 5 calls |
| Optim | 4 calls |
| Qfunction | 3 calls |

## How to Explore

1. `gitnexus_context({name: "PPQuantFunction_toInt"})` — see callers and callees
2. `gitnexus_query({query: "algorithm"})` — find related execution flows
3. Read key files listed above for implementation details
