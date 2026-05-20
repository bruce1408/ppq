---
name: executor
description: "Skill for the Executor area of ppq. 25 symbols across 4 files."
---

# Executor

25 symbols | 4 files | Cohesion: 87%

## When to Use

- Working with code in `ppq/`
- Understanding how RuntimeHook, QuantOPRuntimeHook, TorchMetaDataTracingHook work
- Modifying executor-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/executor/torch.py` | __init__, deploy, to, load_graph, dummy_forward (+6) |
| `ppq/executor/base.py` | __init__, load_graph, RuntimeHook, QuantOPRuntimeHook, __init__ (+3) |
| `ppq/quantization/analyse/graphwise.py` | OutputRecorder, DetailedRecorder, __init__, __init__ |
| `ppq/quantization/observer/__init__.py` | CalibrationHook, __init__ |

## Entry Points

Start here when exploring this area:

- **`RuntimeHook`** (Class) — `ppq/executor/base.py:43`
- **`QuantOPRuntimeHook`** (Class) — `ppq/executor/base.py:75`
- **`TorchMetaDataTracingHook`** (Class) — `ppq/executor/torch.py:15`
- **`OutputRecorder`** (Class) — `ppq/quantization/analyse/graphwise.py:14`
- **`DetailedRecorder`** (Class) — `ppq/quantization/analyse/graphwise.py:38`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `RuntimeHook` | Class | `ppq/executor/base.py` | 43 |
| `QuantOPRuntimeHook` | Class | `ppq/executor/base.py` | 75 |
| `TorchMetaDataTracingHook` | Class | `ppq/executor/torch.py` | 15 |
| `OutputRecorder` | Class | `ppq/quantization/analyse/graphwise.py` | 14 |
| `DetailedRecorder` | Class | `ppq/quantization/analyse/graphwise.py` | 38 |
| `CalibrationHook` | Class | `ppq/quantization/observer/__init__.py` | 39 |
| `BaseGraphExecutor` | Class | `ppq/executor/base.py` | 104 |
| `TorchExecutor` | Class | `ppq/executor/torch.py` | 75 |
| `load_graph` | Method | `ppq/executor/base.py` | 118 |
| `deploy` | Method | `ppq/executor/torch.py` | 349 |
| `to` | Method | `ppq/executor/torch.py` | 358 |
| `load_graph` | Method | `ppq/executor/torch.py` | 603 |
| `dummy_forward` | Method | `ppq/executor/torch.py` | 614 |
| `prepare_input` | Method | `ppq/executor/base.py` | 124 |
| `forward_with_gradient` | Method | `ppq/executor/torch.py` | 411 |
| `quantize_function` | Method | `ppq/executor/torch.py` | 609 |
| `__init__` | Method | `ppq/executor/base.py` | 111 |
| `__init__` | Method | `ppq/executor/torch.py` | 76 |
| `__init__` | Method | `ppq/executor/base.py` | 49 |
| `__init__` | Method | `ppq/executor/base.py` | 82 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Finetune → Is_activated` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Quantize_torch_model → Is_activated` | cross_community | 6 |
| `Quantize_native_model → Prepare_input` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Correct_bias → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Qfunction | 1 calls |
| IR | 1 calls |
| Analyse | 1 calls |

## How to Explore

1. `gitnexus_context({name: "RuntimeHook"})` — see callers and callees
2. `gitnexus_query({query: "executor"})` — find related execution flows
3. Read key files listed above for implementation details
