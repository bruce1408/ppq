---
name: lenet-demo
description: "Skill for the Lenet_demo area of ppq. 12 symbols across 3 files."
---

# Lenet_demo

12 symbols | 3 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how loadWeights, setDynamicRange, fin work
- Modifying lenet_demo-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | loadWeights, setDynamicRange, fin, quant_param, createLenetEngine (+1) |
| `ppq/samples/TensorRT/lenet_demo/generate_onnx.py` | export_onnx, print_onnx_model, main |
| `ppq/samples/TensorRT/lenet_demo/lenet_int8.py` | GiB, generateLenetEngine, setDynamicRange |

## Entry Points

Start here when exploring this area:

- **`loadWeights`** (Function) — `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp:26`
- **`setDynamicRange`** (Function) — `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp:67`
- **`fin`** (Function) — `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp:71`
- **`quant_param`** (Function) — `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp:142`
- **`export_onnx`** (Function) — `ppq/samples/TensorRT/lenet_demo/generate_onnx.py:36`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `loadWeights` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | 26 |
| `setDynamicRange` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | 67 |
| `fin` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | 71 |
| `quant_param` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | 142 |
| `export_onnx` | Function | `ppq/samples/TensorRT/lenet_demo/generate_onnx.py` | 36 |
| `print_onnx_model` | Function | `ppq/samples/TensorRT/lenet_demo/generate_onnx.py` | 43 |
| `main` | Function | `ppq/samples/TensorRT/lenet_demo/generate_onnx.py` | 53 |
| `GiB` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.py` | 16 |
| `generateLenetEngine` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.py` | 19 |
| `setDynamicRange` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.py` | 126 |
| `createLenetEngine` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | 139 |
| `main` | Function | `ppq/samples/TensorRT/lenet_demo/lenet_int8.cpp` | 305 |

## How to Explore

1. `gitnexus_context({name: "loadWeights"})` — see callers and callees
2. `gitnexus_query({query: "lenet_demo"})` — find related execution flows
3. Read key files listed above for implementation details
