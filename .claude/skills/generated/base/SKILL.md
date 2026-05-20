---
name: base
description: "Skill for the Base area of ppq. 82 symbols across 10 files."
---

# Base

82 symbols | 10 files | Cohesion: 81%

## When to Use

- Working with code in `ppq/`
- Understanding how CHECK_OPSET, Clip_Socket, GatherElements_Socket work
- Modifying base-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/IR/base/opdef.py` | CHECK_OPSET, Clip_Socket, GatherElements_Socket, NonZero_Socket, Range_Socket (+27) |
| `ppq/IR/base/command.py` | GraphCommand, GraphDeployCommand, QuantizeOperationCommand, ReplaceOperationCommand, ReplaceVariableCommand (+9) |
| `ppq/IR/base/graph.py` | Variable, BaseGraph, __init__, __init__, dtype (+9) |
| `ppq/IR/quantize.py` | QuantableVariable, __init__, copy, __init__, __init__ (+4) |
| `ppq/core/storage.py` | Serializable, ValueState, __init__, __getstate__ |
| `ppq/core/quant.py` | TensorQuantizationConfig, ChannelwiseTensorQuantizationConfig, copy |
| `ppq/IR/search.py` | TraversalCommand, __init__ |
| `ppq/core/data.py` | convert_from_torch, parsing_from_torch_tensor |
| `ppq/parser/onnx_exporter.py` | build_variable_proto |
| `ppq/executor/op/torch/default.py` | Gemm_forward |

## Entry Points

Start here when exploring this area:

- **`CHECK_OPSET`** (Function) — `ppq/IR/base/opdef.py:176`
- **`Clip_Socket`** (Function) — `ppq/IR/base/opdef.py:454`
- **`GatherElements_Socket`** (Function) — `ppq/IR/base/opdef.py:505`
- **`NonZero_Socket`** (Function) — `ppq/IR/base/opdef.py:590`
- **`Range_Socket`** (Function) — `ppq/IR/base/opdef.py:610`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `GraphCommand` | Class | `ppq/IR/base/command.py` | 113 |
| `GraphDeployCommand` | Class | `ppq/IR/base/command.py` | 124 |
| `QuantizeOperationCommand` | Class | `ppq/IR/base/command.py` | 138 |
| `ReplaceOperationCommand` | Class | `ppq/IR/base/command.py` | 146 |
| `ReplaceVariableCommand` | Class | `ppq/IR/base/command.py` | 153 |
| `TruncateGraphCommand` | Class | `ppq/IR/base/command.py` | 160 |
| `TraversalCommand` | Class | `ppq/IR/search.py` | 80 |
| `Variable` | Class | `ppq/IR/base/graph.py` | 14 |
| `BaseGraph` | Class | `ppq/IR/base/graph.py` | 228 |
| `QuantableVariable` | Class | `ppq/IR/quantize.py` | 183 |
| `TensorQuantizationConfig` | Class | `ppq/core/quant.py` | 366 |
| `ChannelwiseTensorQuantizationConfig` | Class | `ppq/core/quant.py` | 898 |
| `Serializable` | Class | `ppq/core/storage.py` | 27 |
| `ValueState` | Class | `ppq/core/storage.py` | 62 |
| `Operation` | Class | `ppq/IR/base/graph.py` | 156 |
| `OperationBase` | Class | `ppq/IR/base/opdef.py` | 43 |
| `QuantableOperation` | Class | `ppq/IR/quantize.py` | 14 |
| `DeviceSwitchOP` | Class | `ppq/IR/quantize.py` | 245 |
| `CHECK_OPSET` | Function | `ppq/IR/base/opdef.py` | 176 |
| `Clip_Socket` | Function | `ppq/IR/base/opdef.py` | 454 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Process → Copy` | cross_community | 5 |
| `Truncate_graph → Copy` | cross_community | 5 |
| `Export → Convert_from_torch` | cross_community | 4 |
| `Process → Copy` | cross_community | 4 |
| `Fuse_selfattention → Copy` | cross_community | 3 |
| `Fuse_layernorm → Copy` | cross_community | 3 |
| `Fuse_gelu → Copy` | cross_community | 3 |
| `Fuse_skiplayernorm → Copy` | cross_community | 3 |
| `Fuse_gemm → Copy` | cross_community | 3 |

## Connected Areas

| Area | Connections |
|------|-------------|
| IR | 2 calls |

## How to Explore

1. `gitnexus_context({name: "CHECK_OPSET"})` — see callers and callees
2. `gitnexus_query({query: "base"})` — find related execution flows
3. Read key files listed above for implementation details
