---
name: api
description: "Skill for the Api area of ppq. 34 symbols across 9 files."
---

# Api

34 symbols | 9 files | Cohesion: 81%

## When to Use

- Working with code in `ppq/`
- Understanding how quantize_onnx_model, quantize_caffe_model, quantize_native_model work
- Modifying api-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/api/interface.py` | quantize_onnx_model, quantize_caffe_model, quantize_native_model, dispatch_graph, convert_to_daddy_setting (+12) |
| `ppq/api/fsys.py` | dump_to_file, create_dir, dump_internal_results, split_result_to_directory, load_from_file (+1) |
| `ppq/api/setting.py` | default_setting, from_json, assign |
| `ppq/core/quant.py` | __init__, __create_hash, __init__ |
| `ppq/executor/torch.py` | tracing_operation_meta |
| `ppq/core/defs.py` | ppq_warning |
| `ppq/core/ffi.py` | complie |
| `ppq/core/storage.py` | __setstate__ |
| `ppq/quantization/analyse/util/__init__.py` | print |

## Entry Points

Start here when exploring this area:

- **`quantize_onnx_model`** (Function) — `ppq/api/interface.py:184`
- **`quantize_caffe_model`** (Function) — `ppq/api/interface.py:348`
- **`quantize_native_model`** (Function) — `ppq/api/interface.py:452`
- **`dispatch_graph`** (Function) — `ppq/api/interface.py:643`
- **`quantize`** (Function) — `ppq/api/interface.py:804`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `quantize_onnx_model` | Function | `ppq/api/interface.py` | 184 |
| `quantize_caffe_model` | Function | `ppq/api/interface.py` | 348 |
| `quantize_native_model` | Function | `ppq/api/interface.py` | 452 |
| `dispatch_graph` | Function | `ppq/api/interface.py` | 643 |
| `quantize` | Function | `ppq/api/interface.py` | 804 |
| `ppq_warning` | Function | `ppq/core/defs.py` | 99 |
| `load_graph` | Function | `ppq/api/interface.py` | 27 |
| `load_onnx_graph` | Function | `ppq/api/interface.py` | 38 |
| `load_caffe_graph` | Function | `ppq/api/interface.py` | 51 |
| `load_native_graph` | Function | `ppq/api/interface.py` | 65 |
| `format_graph` | Function | `ppq/api/interface.py` | 592 |
| `load_torch_model` | Function | `ppq/api/interface.py` | 77 |
| `dump_torch_to_onnx` | Function | `ppq/api/interface.py` | 138 |
| `quantize_torch_model` | Function | `ppq/api/interface.py` | 278 |
| `export_ppq_graph` | Function | `ppq/api/interface.py` | 545 |
| `export` | Function | `ppq/api/interface.py` | 851 |
| `dump_to_file` | Function | `ppq/api/fsys.py` | 125 |
| `create_dir` | Function | `ppq/api/fsys.py` | 145 |
| `dump_internal_results` | Function | `ppq/api/fsys.py` | 196 |
| `split_result_to_directory` | Function | `ppq/api/fsys.py` | 237 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Quantize_torch_model → Append_variable` | cross_community | 8 |
| `Load_torch_model → Append_variable` | cross_community | 7 |
| `Quantize_torch_model → Append_operation` | cross_community | 6 |
| `Quantize_torch_model → Is_activated` | cross_community | 6 |
| `Quantize_native_model → Prepare_input` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Export → Is_activated` | cross_community | 6 |
| `Quantize → Is_activated` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Analyse | 2 calls |
| Executor | 1 calls |
| Base | 1 calls |
| Algorithm | 1 calls |
| IR | 1 calls |

## How to Explore

1. `gitnexus_context({name: "quantize_onnx_model"})` — see callers and callees
2. `gitnexus_query({query: "api"})` — find related execution flows
3. Read key files listed above for implementation details
