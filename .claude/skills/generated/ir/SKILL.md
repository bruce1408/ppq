---
name: ir
description: "Skill for the IR area of ppq. 152 symbols across 25 files."
---

# IR

152 symbols | 25 files | Cohesion: 87%

## When to Use

- Working with code in `ppq/`
- Understanding how is_linked, truncate_graph, ppq_tensor_round work
- Modifying ir-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/IR/morph.py` | truncate_on_var, delete_isolated, format_parameter, __delete_constant_input, process (+36) |
| `ppq/IR/search.py` | add, match_burte_force, is_linked, _path_matching, _opset_matching (+17) |
| `ppq/IR/base/graph.py` | append_operation, append_variable, get_downstream_operations, get_upstream_operations, topological_sort (+13) |
| `ppq/parser/onnxruntime_exporter.py` | TQC_Exportable_Check, infer_qtype, insert_quantize_node, insert_dequantize_node, remove_activation_ops (+5) |
| `ppq/IR/deploy.py` | RunnableGraph, process, __enter__, __exit__, retrieve (+2) |
| `ppq/IR/processer.py` | GraphCommandProcessor, DefaultGraphProcessor, _acceptable_command_types, __call__, acceptable_command_types (+2) |
| `ppq/quantization/optim/morph.py` | h_split, optimize, delete_hidden_vec, optimize, optimize |
| `ppq/quantization/optim/refine.py` | is_same_platform, optimize, optimize, optimize, optimize |
| `ppq/IR/training.py` | TrainableGraph, parameters, zero_grad, state_dict, __init__ |
| `ppq/core/data.py` | to_torch, create_tensor, convert_from_numpy, parsing_from_numpy_ndarray, convert_any_to_torch_tensor |

## Entry Points

Start here when exploring this area:

- **`is_linked`** (Function) — `ppq/IR/search.py:323`
- **`truncate_graph`** (Function) — `ppq/utils/graph_editor.py:5`
- **`ppq_tensor_round`** (Function) — `ppq/utils/round.py:96`
- **`limitation`** (Function) — `ppq/quantization/optim/ssd.py:77`
- **`output_ops`** (Function) — `ppq/samples/QuantZoo/QuantZoo_Pose.py:70`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `RunnableGraph` | Class | `ppq/IR/deploy.py` | 12 |
| `GraphReplacer` | Class | `ppq/IR/morph.py` | 15 |
| `GraphFormatter` | Class | `ppq/IR/morph.py` | 154 |
| `GraphMerger` | Class | `ppq/IR/morph.py` | 500 |
| `GraphDecomposer` | Class | `ppq/IR/morph.py` | 1077 |
| `GraphDeviceSwitcher` | Class | `ppq/IR/morph.py` | 1160 |
| `GraphCommandProcessor` | Class | `ppq/IR/processer.py` | 8 |
| `DefaultGraphProcessor` | Class | `ppq/IR/processer.py` | 180 |
| `QuantableGraph` | Class | `ppq/IR/quantize.py` | 258 |
| `SearchableGraph` | Class | `ppq/IR/search.py` | 389 |
| `TrainableGraph` | Class | `ppq/IR/training.py` | 10 |
| `is_linked` | Function | `ppq/IR/search.py` | 323 |
| `truncate_graph` | Function | `ppq/utils/graph_editor.py` | 5 |
| `ppq_tensor_round` | Function | `ppq/utils/round.py` | 96 |
| `limitation` | Function | `ppq/quantization/optim/ssd.py` | 77 |
| `output_ops` | Function | `ppq/samples/QuantZoo/QuantZoo_Pose.py` | 70 |
| `Cast_forward` | Function | `ppq/executor/op/torch/default.py` | 1259 |
| `convert_any_to_torch_tensor` | Function | `ppq/core/data.py` | 265 |
| `optimize` | Method | `ProgramEntrance_2.py` | 187 |
| `append_operation` | Method | `ppq/IR/base/graph.py` | 291 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Quantize_torch_model → Append_variable` | cross_community | 8 |
| `Load_torch_model → Append_variable` | cross_community | 7 |
| `Optimize → Get_upstream_operations` | cross_community | 6 |
| `Optimize → Get_downstream_operations` | cross_community | 6 |
| `Optimize → Add` | cross_community | 6 |
| `Quantize_torch_model → Append_operation` | cross_community | 6 |
| `Process → Copy` | cross_community | 5 |
| `Process → Remove_variable` | cross_community | 5 |
| `Process → Mark_variable_as_graph_output` | cross_community | 5 |
| `Export → Get_upstream_operations` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Algorithm | 20 calls |
| Parser | 8 calls |
| Base | 2 calls |
| Observer | 2 calls |
| Qfunction | 1 calls |
| Optim | 1 calls |

## How to Explore

1. `gitnexus_context({name: "is_linked"})` — see callers and callees
2. `gitnexus_query({query: "ir"})` — find related execution flows
3. Read key files listed above for implementation details
