---
name: caffe
description: "Skill for the Caffe area of ppq. 157 symbols across 7 files."
---

# Caffe

157 symbols | 7 files | Cohesion: 94%

## When to Use

- Working with code in `ppq/`
- Understanding how convert_any_to_python_primary_type, refine_value, build_temp_graph work
- Modifying caffe-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/parser/caffe/caffe_export_utils.py` | CaffeOpExporter, Conv, BatchNormalization, Relu, PRelu (+79) |
| `ppq/parser/caffe/caffe_import_utils.py` | CaffeOpBuilder, Convolution, BatchNorm, BN, Deconvolution (+56) |
| `ppq/core/data.py` | convert_any_to_python_primary_type, convert_any_to_numpy, convert_any_to_string, to_numpy, create_ndarray |
| `ppq/parser/caffe/caffe_graph_optim.py` | de_inplace, new_name, merge_batchnorm_scale |
| `ppq/parser/caffe_parser.py` | load_graph_and_format, build |
| `ppq/IR/base/graph.py` | set_extension_attrib |
| `ppq/core/storage.py` | __init__ |

## Entry Points

Start here when exploring this area:

- **`convert_any_to_python_primary_type`** (Function) — `ppq/core/data.py:224`
- **`refine_value`** (Function) — `ppq/parser/caffe/caffe_export_utils.py:16`
- **`build_temp_graph`** (Function) — `ppq/parser/caffe/caffe_import_utils.py:19`
- **`convert_any_to_numpy`** (Function) — `ppq/core/data.py:248`
- **`convert_any_to_string`** (Function) — `ppq/core/data.py:301`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `CaffeOpBuilder` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 118 |
| `Convolution` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 226 |
| `BatchNorm` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 255 |
| `BN` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 303 |
| `Deconvolution` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 316 |
| `ReLU` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 321 |
| `PReLU` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 337 |
| `Concat` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 350 |
| `Softmax` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 358 |
| `Transpose` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 366 |
| `ReduceL2` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 374 |
| `Reduce` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 383 |
| `Div` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 394 |
| `Pooling` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 399 |
| `Eltwise` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 447 |
| `Reshape` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 513 |
| `ReLU6` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 525 |
| `Clip` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 531 |
| `Mul` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 538 |
| `Add` | Class | `ppq/parser/caffe/caffe_import_utils.py` | 542 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Is_activated` | cross_community | 6 |
| `Trans → Prepare_input` | cross_community | 5 |
| `Trans → Prepare_input` | cross_community | 5 |
| `Trans → Prepare_input` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Base | 1 calls |
| Analyse | 1 calls |

## How to Explore

1. `gitnexus_context({name: "convert_any_to_python_primary_type"})` — see callers and callees
2. `gitnexus_query({query: "caffe"})` — find related execution flows
3. Read key files listed above for implementation details
