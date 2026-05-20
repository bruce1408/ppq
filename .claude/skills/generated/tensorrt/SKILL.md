---
name: tensorrt
description: "Skill for the TensorRT area of ppq. 12 symbols across 3 files."
---

# TensorRT

12 symbols | 3 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how GiB, json_load, setDynamicRange work
- Modifying tensorrt-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/samples/TensorRT/trt_infer.py` | allocate_buffers, do_inference, find_sample_data, get_data_path, locate_files (+2) |
| `ppq/samples/TensorRT/create_engine.py` | GiB, json_load, setDynamicRange, build_engine |
| `ppq/samples/TensorRT/Benchmark_with_onnx.py` | infer_trt |

## Entry Points

Start here when exploring this area:

- **`GiB`** (Function) — `ppq/samples/TensorRT/create_engine.py:9`
- **`json_load`** (Function) — `ppq/samples/TensorRT/create_engine.py:12`
- **`setDynamicRange`** (Function) — `ppq/samples/TensorRT/create_engine.py:17`
- **`build_engine`** (Function) — `ppq/samples/TensorRT/create_engine.py:46`
- **`infer_trt`** (Function) — `ppq/samples/TensorRT/Benchmark_with_onnx.py:26`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `GiB` | Function | `ppq/samples/TensorRT/create_engine.py` | 9 |
| `json_load` | Function | `ppq/samples/TensorRT/create_engine.py` | 12 |
| `setDynamicRange` | Function | `ppq/samples/TensorRT/create_engine.py` | 17 |
| `build_engine` | Function | `ppq/samples/TensorRT/create_engine.py` | 46 |
| `infer_trt` | Function | `ppq/samples/TensorRT/Benchmark_with_onnx.py` | 26 |
| `allocate_buffers` | Function | `ppq/samples/TensorRT/trt_infer.py` | 124 |
| `do_inference` | Function | `ppq/samples/TensorRT/trt_infer.py` | 146 |
| `find_sample_data` | Function | `ppq/samples/TensorRT/trt_infer.py` | 47 |
| `get_data_path` | Function | `ppq/samples/TensorRT/trt_infer.py` | 66 |
| `locate_files` | Function | `ppq/samples/TensorRT/trt_infer.py` | 81 |
| `__str__` | Method | `ppq/samples/TensorRT/trt_infer.py` | 117 |
| `__repr__` | Method | `ppq/samples/TensorRT/trt_infer.py` | 120 |

## How to Explore

1. `gitnexus_context({name: "GiB"})` — see callers and callees
2. `gitnexus_query({query: "tensorrt"})` — find related execution flows
3. Read key files listed above for implementation details
