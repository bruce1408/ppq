---
name: observer
description: "Skill for the Observer area of ppq. 43 symbols across 9 files."
---

# Observer

43 symbols | 9 files | Cohesion: 92%

## When to Use

- Working with code in `ppq/`
- Understanding how minmax_to_scale_offset, ppq_numerical_round, ppq_round_to_power_of_2 work
- Modifying observer-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/quantization/observer/range.py` | minmax_to_scale_offset, render_quantization_config, hist_to_scale_offset, render_quantization_config, render_quantization_config (+13) |
| `ppq/lib/quant.py` | Observer, __init__, observe, render, __init__ |
| `ppq/core/ffi.py` | compute_mse_loss, Histogram_T, Histogram_Asymmetric_T, Quantile |
| `ppq/quantization/observer/floating.py` | ConstantObserver, DirectMSEObserver, __init__, __init__ |
| `ppq/quantization/observer/order.py` | render_quantization_config, TorchIsotoneObserver, __init__ |
| `ppq/quantization/observer/__init__.py` | build_observer, __init__, build_hook |
| `ppq/quantization/qfunction/linear.py` | forward, forward |
| `ppq/utils/round.py` | ppq_numerical_round, ppq_round_to_power_of_2 |
| `ppq/quantization/observer/base.py` | BaseTensorObserver, __init__ |

## Entry Points

Start here when exploring this area:

- **`minmax_to_scale_offset`** (Function) — `ppq/quantization/observer/range.py:22`
- **`ppq_numerical_round`** (Function) — `ppq/utils/round.py:50`
- **`ppq_round_to_power_of_2`** (Function) — `ppq/utils/round.py:114`
- **`Observer`** (Function) — `ppq/lib/quant.py:46`
- **`BaseTensorObserver`** (Class) — `ppq/quantization/observer/base.py:8`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `BaseTensorObserver` | Class | `ppq/quantization/observer/base.py` | 8 |
| `ConstantObserver` | Class | `ppq/quantization/observer/floating.py` | 10 |
| `DirectMSEObserver` | Class | `ppq/quantization/observer/floating.py` | 50 |
| `TorchIsotoneObserver` | Class | `ppq/quantization/observer/order.py` | 11 |
| `TorchMinMaxObserver` | Class | `ppq/quantization/observer/range.py` | 77 |
| `TorchHistObserver` | Class | `ppq/quantization/observer/range.py` | 139 |
| `TorchPercentileObserver` | Class | `ppq/quantization/observer/range.py` | 311 |
| `TorchMSEObserver` | Class | `ppq/quantization/observer/range.py` | 405 |
| `minmax_to_scale_offset` | Function | `ppq/quantization/observer/range.py` | 22 |
| `ppq_numerical_round` | Function | `ppq/utils/round.py` | 50 |
| `ppq_round_to_power_of_2` | Function | `ppq/utils/round.py` | 114 |
| `Observer` | Function | `ppq/lib/quant.py` | 46 |
| `compute_mse_loss` | Method | `ppq/core/ffi.py` | 263 |
| `render_quantization_config` | Method | `ppq/quantization/observer/order.py` | 59 |
| `render_quantization_config` | Method | `ppq/quantization/observer/range.py` | 101 |
| `hist_to_scale_offset` | Method | `ppq/quantization/observer/range.py` | 190 |
| `render_quantization_config` | Method | `ppq/quantization/observer/range.py` | 283 |
| `render_quantization_config` | Method | `ppq/quantization/observer/range.py` | 359 |
| `compute_mse_loss` | Method | `ppq/quantization/observer/range.py` | 421 |
| `hist_to_scale_offset` | Method | `ppq/quantization/observer/range.py` | 456 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Optimize → Has_property` | cross_community | 4 |
| `Optimize → Ppq_numerical_round` | cross_community | 4 |
| `Hist_to_scale_offset → Compute_mse_loss` | intra_community | 3 |
| `Forward → Has_property` | cross_community | 3 |
| `Forward → Ppq_numerical_round` | intra_community | 3 |
| `Forward → Has_property` | cross_community | 3 |
| `Forward → Ppq_numerical_round` | intra_community | 3 |
| `Hist_to_scale_offset → Ppq_numerical_round` | intra_community | 3 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Algorithm | 12 calls |
| IR | 2 calls |

## How to Explore

1. `gitnexus_context({name: "minmax_to_scale_offset"})` — see callers and callees
2. `gitnexus_query({query: "observer"})` — find related execution flows
3. Read key files listed above for implementation details
