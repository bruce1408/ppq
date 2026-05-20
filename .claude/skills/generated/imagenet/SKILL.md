---
name: imagenet
description: "Skill for the Imagenet area of ppq. 7 symbols across 1 files."
---

# Imagenet

7 symbols | 1 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how accuracy, load_imagenet_from_directory, evaluate_torch_module_with_imagenet work
- Modifying imagenet-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | accuracy, load_imagenet_from_directory, evaluate_torch_module_with_imagenet, evaluate_onnx_module_with_imagenet, evaluate_mmlab_module_with_imagenet (+2) |

## Entry Points

Start here when exploring this area:

- **`accuracy`** (Function) — `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py:18`
- **`load_imagenet_from_directory`** (Function) — `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py:36`
- **`evaluate_torch_module_with_imagenet`** (Function) — `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py:80`
- **`evaluate_onnx_module_with_imagenet`** (Function) — `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py:95`
- **`evaluate_mmlab_module_with_imagenet`** (Function) — `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py:114`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `accuracy` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 18 |
| `load_imagenet_from_directory` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 36 |
| `evaluate_torch_module_with_imagenet` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 80 |
| `evaluate_onnx_module_with_imagenet` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 95 |
| `evaluate_mmlab_module_with_imagenet` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 114 |
| `evaluate_ppq_module_with_imagenet` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 130 |
| `_evaluate_any_module_with_imagenet` | Function | `ppq/samples/Imagenet/Utilities/Imagenet/imagenet_util.py` | 151 |

## How to Explore

1. `gitnexus_context({name: "accuracy"})` — see callers and callees
2. `gitnexus_query({query: "imagenet"})` — find related execution flows
3. Read key files listed above for implementation details
