---
name: analyse
description: "Skill for the Analyse area of ppq. 22 symbols across 9 files."
---

# Analyse

22 symbols | 9 files | Cohesion: 84%

## When to Use

- Working with code in `ppq/`
- Understanding how generate_indexer, generate_torch_indexer, tensor_random_fetch work
- Modifying analyse-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/quantization/analyse/graphwise.py` | pre_forward_hook, post_forward_hook, pre_forward_hook, post_forward_hook, graphwise_error_analyse (+4) |
| `ppq/utils/fetch.py` | generate_indexer, generate_torch_indexer, tensor_random_fetch, channel_random_fetch, batch_random_fetch |
| `ppq/executor/base.py` | pre_forward_hook, post_forward_hook |
| `ppq/quantization/algorithm/training.py` | push |
| `ppq/quantization/observer/floating.py` | observe |
| `ppq/executor/torch.py` | forward |
| `ppq/quantization/analyse/layerwise.py` | layerwise_error_analyse |
| `ppq/samples/QuantZoo/QuantZoo_SuperRes.py` | evaluation |
| `ppq/quantization/measure/norm.py` | torch_snr_error |

## Entry Points

Start here when exploring this area:

- **`generate_indexer`** (Function) — `ppq/utils/fetch.py:3`
- **`generate_torch_indexer`** (Function) — `ppq/utils/fetch.py:25`
- **`tensor_random_fetch`** (Function) — `ppq/utils/fetch.py:31`
- **`channel_random_fetch`** (Function) — `ppq/utils/fetch.py:52`
- **`batch_random_fetch`** (Function) — `ppq/utils/fetch.py:82`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `generate_indexer` | Function | `ppq/utils/fetch.py` | 3 |
| `generate_torch_indexer` | Function | `ppq/utils/fetch.py` | 25 |
| `tensor_random_fetch` | Function | `ppq/utils/fetch.py` | 31 |
| `channel_random_fetch` | Function | `ppq/utils/fetch.py` | 52 |
| `batch_random_fetch` | Function | `ppq/utils/fetch.py` | 82 |
| `graphwise_error_analyse` | Function | `ppq/quantization/analyse/graphwise.py` | 63 |
| `statistical_analyse` | Function | `ppq/quantization/analyse/graphwise.py` | 185 |
| `layerwise_error_analyse` | Function | `ppq/quantization/analyse/layerwise.py` | 14 |
| `evaluation` | Function | `ppq/samples/QuantZoo/QuantZoo_SuperRes.py` | 65 |
| `torch_snr_error` | Function | `ppq/quantization/measure/norm.py` | 51 |
| `pre_forward_hook` | Method | `ppq/executor/base.py` | 52 |
| `post_forward_hook` | Method | `ppq/executor/base.py` | 63 |
| `push` | Method | `ppq/quantization/algorithm/training.py` | 111 |
| `pre_forward_hook` | Method | `ppq/quantization/analyse/graphwise.py` | 20 |
| `post_forward_hook` | Method | `ppq/quantization/analyse/graphwise.py` | 23 |
| `pre_forward_hook` | Method | `ppq/quantization/analyse/graphwise.py` | 46 |
| `post_forward_hook` | Method | `ppq/quantization/analyse/graphwise.py` | 52 |
| `observe` | Method | `ppq/quantization/observer/floating.py` | 75 |
| `forward` | Method | `ppq/executor/torch.py` | 365 |
| `stat` | Method | `ppq/quantization/analyse/graphwise.py` | 224 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Executor | 1 calls |

## How to Explore

1. `gitnexus_context({name: "generate_indexer"})` — see callers and callees
2. `gitnexus_query({query: "analyse"})` — find related execution flows
3. Read key files listed above for implementation details
