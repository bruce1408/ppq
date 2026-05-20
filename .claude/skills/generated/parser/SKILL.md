---
name: parser
description: "Skill for the Parser area of ppq. 91 symbols across 23 files."
---

# Parser

91 symbols | 23 files | Cohesion: 86%

## When to Use

- Working with code in `ppq/`
- Understanding how optimize_for_export, slice_combine, eltwise_combine work
- Modifying parser-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/parser/caffe_exporter.py` | convert_type, export_quantization_config, prepare_model, dump_to_file, export (+8) |
| `ppq/parser/onnx_exporter.py` | ConstantOfShapeExporter, MMCVExporter, InterpExporter, OOSExporter, AttentionExporter (+8) |
| `ppq/parser/tengine_exporter.py` | TengineExporter, ConstantOfShapeExporter, MMCVExporter, InterpExporter, OOSExporter (+5) |
| `ppq/parser/onnx_parser.py` | build_variables, initialize_params, de_inplace, new_name, refine_graph (+3) |
| `ppq/parser/ascend_export.py` | AscendExporter, export, adapt_scale, check_offset, generate_shape (+1) |
| `ppq/parser/native.py` | NativeExporter, NativeImporter, export, dump_elements_to_file, build (+1) |
| `ppq/parser/nxp_exporter.py` | NxpExporter, export_operation, export_var, export |
| `ppq/parser/caffe/caffe_graph_optim.py` | optimize_for_export, slice_combine, eltwise_combine |
| `ppq/parser/ppl.py` | convert_type, export_quantization_config, PPLBackendExporter |
| `ppq/IR/base/graph.py` | GraphExporter, OperationExporter, GraphBuilder |

## Entry Points

Start here when exploring this area:

- **`optimize_for_export`** (Function) — `ppq/parser/caffe/caffe_graph_optim.py:98`
- **`slice_combine`** (Function) — `ppq/parser/caffe/caffe_graph_optim.py:106`
- **`eltwise_combine`** (Function) — `ppq/parser/caffe/caffe_graph_optim.py:167`
- **`convert_type`** (Function) — `ppq/parser/caffe_exporter.py:21`
- **`convert_type`** (Function) — `ppq/parser/ppl.py:11`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `MyExporter` | Class | `ProgramEntrance_2.py` | 34 |
| `GraphExporter` | Class | `ppq/IR/base/graph.py` | 928 |
| `AscendExporter` | Class | `ppq/parser/ascend_export.py` | 45 |
| `ExtensionExporter` | Class | `ppq/parser/extension.py` | 5 |
| `MNNExporter` | Class | `ppq/parser/mnn_exporter.py` | 10 |
| `NativeExporter` | Class | `ppq/parser/native.py` | 7 |
| `NCNNExporter` | Class | `ppq/parser/ncnn_exporter.py` | 12 |
| `NxpExporter` | Class | `ppq/parser/nxp_exporter.py` | 9 |
| `QNNDSPExporter` | Class | `ppq/parser/qnn_exporter.py` | 14 |
| `TengineExporter` | Class | `ppq/parser/tengine_exporter.py` | 62 |
| `TensorRTExporter_JSON` | Class | `ppq/parser/tensorRT.py` | 55 |
| `OperationExporter` | Class | `ppq/IR/base/graph.py` | 933 |
| `ConstantOfShapeExporter` | Class | `ppq/parser/onnx_exporter.py` | 15 |
| `MMCVExporter` | Class | `ppq/parser/onnx_exporter.py` | 22 |
| `InterpExporter` | Class | `ppq/parser/onnx_exporter.py` | 28 |
| `OOSExporter` | Class | `ppq/parser/onnx_exporter.py` | 34 |
| `AttentionExporter` | Class | `ppq/parser/onnx_exporter.py` | 40 |
| `PPQBiasFusedMatMulExporter` | Class | `ppq/parser/onnx_exporter.py` | 46 |
| `ConstantOfShapeExporter` | Class | `ppq/parser/tengine_exporter.py` | 12 |
| `MMCVExporter` | Class | `ppq/parser/tengine_exporter.py` | 22 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Get_upstream_operations` | cross_community | 5 |
| `Export → Get_downstream_operations` | cross_community | 5 |
| `Export → Get_upstream_operations` | cross_community | 5 |
| `Export → Get_upstream_operations` | cross_community | 5 |
| `Export → Get_downstream_operations` | cross_community | 5 |
| `Export → Get_upstream_operations` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| IR | 8 calls |
| Caffe | 1 calls |
| Qfunction | 1 calls |
| Base | 1 calls |
| Api | 1 calls |

## How to Explore

1. `gitnexus_context({name: "optimize_for_export"})` — see callers and callees
2. `gitnexus_query({query: "parser"})` — find related execution flows
3. Read key files listed above for implementation details
