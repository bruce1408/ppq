---
name: qfunction
description: "Skill for the Qfunction area of ppq. 9 symbols across 4 files."
---

# Qfunction

9 symbols | 4 files | Cohesion: 69%

## When to Use

- Working with code in `ppq/`
- Understanding how PPQFloatingQuantFunction, PPQDyamicLinearQuantFunction, PPQLinearQuantFunction work
- Modifying qfunction-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/quantization/qfunction/floating.py` | PPQFloatingQuantFunction, forward, forward |
| `ppq/core/quant.py` | is_activated, can_export |
| `ppq/quantization/qfunction/linear.py` | PPQDyamicLinearQuantFunction, PPQLinearQuantFunction |
| `ppq/core/ffi.py` | FloatingQuantize_T, FloatingQuantize_C |

## Entry Points

Start here when exploring this area:

- **`PPQFloatingQuantFunction`** (Function) — `ppq/quantization/qfunction/floating.py:94`
- **`PPQDyamicLinearQuantFunction`** (Function) — `ppq/quantization/qfunction/linear.py:174`
- **`PPQLinearQuantFunction`** (Function) — `ppq/quantization/qfunction/linear.py:199`
- **`is_activated`** (Method) — `ppq/core/quant.py:357`
- **`can_export`** (Method) — `ppq/core/quant.py:600`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `PPQFloatingQuantFunction` | Function | `ppq/quantization/qfunction/floating.py` | 94 |
| `PPQDyamicLinearQuantFunction` | Function | `ppq/quantization/qfunction/linear.py` | 174 |
| `PPQLinearQuantFunction` | Function | `ppq/quantization/qfunction/linear.py` | 199 |
| `is_activated` | Method | `ppq/core/quant.py` | 357 |
| `can_export` | Method | `ppq/core/quant.py` | 600 |
| `FloatingQuantize_T` | Method | `ppq/core/ffi.py` | 272 |
| `forward` | Method | `ppq/quantization/qfunction/floating.py` | 20 |
| `FloatingQuantize_C` | Method | `ppq/core/ffi.py` | 290 |
| `forward` | Method | `ppq/quantization/qfunction/floating.py` | 65 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Finetune → Is_activated` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Quantize_torch_model → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Correct_bias → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Algorithm | 12 calls |

## How to Explore

1. `gitnexus_context({name: "PPQFloatingQuantFunction"})` — see callers and callees
2. `gitnexus_query({query: "qfunction"})` — find related execution flows
3. Read key files listed above for implementation details
