---
name: tests
description: "Skill for the Tests area of ppq. 7 symbols across 3 files."
---

# Tests

7 symbols | 3 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how ref_grad_func, LinearQuantize_T_B, LinearQuantize_C_B work
- Modifying tests-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/test_cuda_kernel.py` | __TEST_QUANTIZE_LT_B__, ref_grad_func, __TEST_QUANTIZE_LC_B__ |
| `ppq/core/ffi.py` | LinearQuantize_T_B, LinearQuantize_C_B |
| `ppq/quantization/algorithm/training.py` | backward, backward |

## Entry Points

Start here when exploring this area:

- **`ref_grad_func`** (Function) — `tests/test_cuda_kernel.py:66`
- **`LinearQuantize_T_B`** (Method) — `ppq/core/ffi.py:105`
- **`LinearQuantize_C_B`** (Method) — `ppq/core/ffi.py:120`
- **`backward`** (Method) — `ppq/quantization/algorithm/training.py:40`
- **`backward`** (Method) — `ppq/quantization/algorithm/training.py:78`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `ref_grad_func` | Function | `tests/test_cuda_kernel.py` | 66 |
| `LinearQuantize_T_B` | Method | `ppq/core/ffi.py` | 105 |
| `LinearQuantize_C_B` | Method | `ppq/core/ffi.py` | 120 |
| `backward` | Method | `ppq/quantization/algorithm/training.py` | 40 |
| `backward` | Method | `ppq/quantization/algorithm/training.py` | 78 |
| `__TEST_QUANTIZE_LT_B__` | Function | `tests/test_cuda_kernel.py` | 65 |
| `__TEST_QUANTIZE_LC_B__` | Function | `tests/test_cuda_kernel.py` | 102 |

## How to Explore

1. `gitnexus_context({name: "ref_grad_func"})` — see callers and callees
2. `gitnexus_query({query: "tests"})` — find related execution flows
3. Read key files listed above for implementation details
