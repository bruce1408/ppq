---
name: quantizer
description: "Skill for the Quantizer area of ppq. 92 symbols across 25 files."
---

# Quantizer

92 symbols | 25 files | Cohesion: 96%

## When to Use

- Working with code in `ppq/`
- Understanding how GET_ATTRIBUTE_FROM_OPERATION, ASSERT_CONV_AND_DECONV, ASSERT_GEMM work
- Modifying quantizer-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/quantization/quantizer/base.py` | BaseQuantizer, create_default_quant_config, __init__, quantize, quantize_operation (+4) |
| `ppq/quantization/quantizer/MetaxQuantizer.py` | MetaxTensorwiseQuantizer, MetaxChannelwiseQuantizer, init_quantize_config, init_quantize_config, __init__ (+3) |
| `ppq/quantization/quantizer/DSPQuantizer.py` | PPL_DSP_Quantizer, PPL_DSP_TI_Quantizer, init_quantize_config, init_quantize_config, __init__ (+2) |
| `ppq/quantization/quantizer/FP8Quantizer.py` | GraphCoreQuantizer, TensorRTQuantizer_FP8, init_quantize_config, init_quantize_config, __init__ (+1) |
| `ppq/quantization/quantizer/RKNNQuantizer.py` | RKNN_PerTensorQuantizer, RKNN_PerChannelQuantizer, init_quantize_config, init_quantize_config, __init__ (+1) |
| `ppq/quantization/quantizer/TensorRTQuantizer.py` | TensorRTQuantizer, TensorRTQuantizer_InputOnly, init_quantize_config, init_quantize_config, __init__ (+1) |
| `ppq/quantization/quantizer/AscendQuantizer.py` | AscendQuantizer, __init__, ASSERT_CONV_AND_DECONV, ASSERT_GEMM, init_quantize_config |
| `ppq/quantization/quantizer/FPGAQuantizer.py` | FPGAQuantizer, init_quantize_config, __init__, build_quant_pipeline |
| `ppq/quantization/quantizer/NCNNQuantizer.py` | NCNNQuantizer, init_quantize_config, __init__, build_prequant_pipeline |
| `ppq/quantization/quantizer/NXPQuantizer.py` | NXP_Quantizer, init_quantize_config, __init__, build_quant_pipeline |

## Entry Points

Start here when exploring this area:

- **`GET_ATTRIBUTE_FROM_OPERATION`** (Function) — `ppq/executor/op/torch/base.py:26`
- **`ASSERT_CONV_AND_DECONV`** (Function) — `ppq/quantization/quantizer/AscendQuantizer.py:11`
- **`ASSERT_GEMM`** (Function) — `ppq/quantization/quantizer/AscendQuantizer.py:32`
- **`MyInt8Quantizer`** (Class) — `ProgramEntrance_2.py:63`
- **`AscendQuantizer`** (Class) — `ppq/quantization/quantizer/AscendQuantizer.py:44`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `MyInt8Quantizer` | Class | `ProgramEntrance_2.py` | 63 |
| `AscendQuantizer` | Class | `ppq/quantization/quantizer/AscendQuantizer.py` | 44 |
| `PPL_DSP_Quantizer` | Class | `ppq/quantization/quantizer/DSPQuantizer.py` | 14 |
| `PPL_DSP_TI_Quantizer` | Class | `ppq/quantization/quantizer/DSPQuantizer.py` | 115 |
| `GraphCoreQuantizer` | Class | `ppq/quantization/quantizer/FP8Quantizer.py` | 11 |
| `TensorRTQuantizer_FP8` | Class | `ppq/quantization/quantizer/FP8Quantizer.py` | 106 |
| `FPGAQuantizer` | Class | `ppq/quantization/quantizer/FPGAQuantizer.py` | 13 |
| `MNNQuantizer` | Class | `ppq/quantization/quantizer/MNNQuantizer.py` | 11 |
| `MetaxTensorwiseQuantizer` | Class | `ppq/quantization/quantizer/MetaxQuantizer.py` | 16 |
| `MetaxChannelwiseQuantizer` | Class | `ppq/quantization/quantizer/MetaxQuantizer.py` | 99 |
| `ExtQuantizer` | Class | `ppq/quantization/quantizer/MyQuantizer.py` | 15 |
| `NCNNQuantizer` | Class | `ppq/quantization/quantizer/NCNNQuantizer.py` | 15 |
| `NXP_Quantizer` | Class | `ppq/quantization/quantizer/NXPQuantizer.py` | 15 |
| `OnnxruntimeQuantizer` | Class | `ppq/quantization/quantizer/ORTQuantizer.py` | 11 |
| `OpenvinoQuantizer` | Class | `ppq/quantization/quantizer/OpenvinoQuantizer.py` | 11 |
| `PPLCUDAQuantizer` | Class | `ppq/quantization/quantizer/PPLQuantizer.py` | 11 |
| `RKNN_PerTensorQuantizer` | Class | `ppq/quantization/quantizer/RKNNQuantizer.py` | 11 |
| `RKNN_PerChannelQuantizer` | Class | `ppq/quantization/quantizer/RKNNQuantizer.py` | 89 |
| `TengineQuantizer` | Class | `ppq/quantization/quantizer/TengineQuantizer.py` | 11 |
| `TensorRTQuantizer` | Class | `ppq/quantization/quantizer/TensorRTQuantizer.py` | 11 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Init_quantize_config → GET_ATTRIBUTE_FROM_OPERATION` | intra_community | 3 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Executor | 2 calls |

## How to Explore

1. `gitnexus_context({name: "GET_ATTRIBUTE_FROM_OPERATION"})` — see callers and callees
2. `gitnexus_query({query: "quantizer"})` — find related execution flows
3. Read key files listed above for implementation details
