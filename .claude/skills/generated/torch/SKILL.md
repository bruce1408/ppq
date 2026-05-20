---
name: torch
description: "Skill for the Torch area of ppq. 19 symbols across 4 files."
---

# Torch

19 symbols | 4 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how Squeeze_forward, Unsqueeze_forward, ReduceSum_forward work
- Modifying torch-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/executor/op/torch/default.py` | Squeeze_forward, Unsqueeze_forward, ReduceSum_forward, Split_forward, Softmax_forward (+10) |
| `ppq/IR/base/opdef.py` | onnx_opset_version, set_extension_attrib |
| `ppq/executor/op/torch/base.py` | ASSERT_NUM_OF_INPUT |
| `ppq/executor/op/torch/cuda.py` | AveragePool_forward |

## Entry Points

Start here when exploring this area:

- **`Squeeze_forward`** (Function) — `ppq/executor/op/torch/default.py:983`
- **`Unsqueeze_forward`** (Function) — `ppq/executor/op/torch/default.py:1038`
- **`ReduceSum_forward`** (Function) — `ppq/executor/op/torch/default.py:1651`
- **`Split_forward`** (Function) — `ppq/executor/op/torch/default.py:2022`
- **`Softmax_forward`** (Function) — `ppq/executor/op/torch/default.py:2093`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `Squeeze_forward` | Function | `ppq/executor/op/torch/default.py` | 983 |
| `Unsqueeze_forward` | Function | `ppq/executor/op/torch/default.py` | 1038 |
| `ReduceSum_forward` | Function | `ppq/executor/op/torch/default.py` | 1651 |
| `Split_forward` | Function | `ppq/executor/op/torch/default.py` | 2022 |
| `Softmax_forward` | Function | `ppq/executor/op/torch/default.py` | 2093 |
| `Log_forward` | Function | `ppq/executor/op/torch/default.py` | 2384 |
| `LogSoftmax_forward` | Function | `ppq/executor/op/torch/default.py` | 3403 |
| `convert_onnx_pads_to_torch` | Function | `ppq/executor/op/torch/default.py` | 23 |
| `Conv_forward` | Function | `ppq/executor/op/torch/default.py` | 182 |
| `ConvTranspose_forward` | Function | `ppq/executor/op/torch/default.py` | 325 |
| `MaxPool2d_forward` | Function | `ppq/executor/op/torch/default.py` | 488 |
| `AveragePool_forward` | Function | `ppq/executor/op/torch/default.py` | 761 |
| `Pad_forward` | Function | `ppq/executor/op/torch/default.py` | 2299 |
| `GRU_forward` | Function | `ppq/executor/op/torch/default.py` | 2736 |
| `LSTM_forward` | Function | `ppq/executor/op/torch/default.py` | 2950 |
| `ASSERT_NUM_OF_INPUT` | Function | `ppq/executor/op/torch/base.py` | 13 |
| `AveragePool_forward` | Function | `ppq/executor/op/torch/cuda.py` | 18 |
| `onnx_opset_version` | Method | `ppq/IR/base/opdef.py` | 33 |
| `set_extension_attrib` | Method | `ppq/IR/base/opdef.py` | 126 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `LogSoftmax_forward → Onnx_opset_version` | intra_community | 3 |

## How to Explore

1. `gitnexus_context({name: "Squeeze_forward"})` — see callers and callees
2. `gitnexus_query({query: "torch"})` — find related execution flows
3. Read key files listed above for implementation details
