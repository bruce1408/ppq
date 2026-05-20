---
name: optim
description: "Skill for the Optim area of ppq. 146 symbols across 21 files."
---

# Optim

146 symbols | 21 files | Cohesion: 87%

## When to Use

- Working with code in `ppq/`
- Understanding how variable_analyse, cache_fn, aggregate work
- Modifying optim-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/quantization/optim/training.py` | enable_block_gradient, disable_block_gradient, compute_block_loss, finetune, finetune (+20) |
| `ppq/quantization/optim/ssd.py` | SSDEqualizationPass, __init__, collect_activation_range, layer_weight_norm, prepare_weight_for_equalization (+15) |
| `ppq/quantization/optim/refine.py` | QuantizeSimplifyPass, QuantizeFusionPass, QuantAlignmentPass, SwishFusionPass, MishFusionPass (+13) |
| `ppq/quantization/optim/equalization.py` | ActivationEqualizationPass, LayerwiseEqualizationPass, ChannelwiseSplitPass, __init__, __init__ (+8) |
| `ppq/quantization/optim/legacy.py` | PPLCudaAddConvReluMerge, __init__, tune_block_weight_scale, finetune, optimize (+8) |
| `ppq/quantization/optim/morph.py` | NXPResizeModeChangePass, NCNNFormatGemmPass, HorizontalLayerSplitPass, MetaxGemmSplitPass, GRUSplitPass (+5) |
| `ppq/quantization/optim/calibration.py` | RuntimeCalibrationPass, PPLDSPTIReCalibrationPass, IsotoneCalibrationPass, __init__, __init__ (+4) |
| `ppq/quantization/optim/parameters.py` | PassiveParameterQuantizePass, ParameterQuantizePass, __init__, __init__, optimize (+2) |
| `ppq/quantization/optim/exprimental.py` | MatrixFactorizationPass, __init__, collect_training_data, optimize, LearningToCalibPass (+1) |
| `ppq/quantization/optim/base.py` | QuantizationOptimizationPass, __init__, __init__, append_optimization_to_pipeline |

## Entry Points

Start here when exploring this area:

- **`variable_analyse`** (Function) — `ppq/quantization/analyse/layerwise.py:136`
- **`cache_fn`** (Function) — `ppq/quantization/optim/training.py:250`
- **`aggregate`** (Function) — `ppq/quantization/optim/equalization.py:137`
- **`retrospect`** (Function) — `ppq/quantization/optim/legacy.py:351`
- **`merge_fn`** (Function) — `ppq/quantization/optim/legacy.py:360`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `MyOptimPass` | Class | `ProgramEntrance_2.py` | 172 |
| `ParameterBakingPass` | Class | `ppq/quantization/optim/baking.py` | 10 |
| `QuantizationOptimizationPass` | Class | `ppq/quantization/optim/base.py` | 7 |
| `RuntimeCalibrationPass` | Class | `ppq/quantization/optim/calibration.py` | 18 |
| `PPLDSPTIReCalibrationPass` | Class | `ppq/quantization/optim/calibration.py` | 215 |
| `IsotoneCalibrationPass` | Class | `ppq/quantization/optim/calibration.py` | 324 |
| `ActivationEqualizationPass` | Class | `ppq/quantization/optim/equalization.py` | 22 |
| `LayerwiseEqualizationPass` | Class | `ppq/quantization/optim/equalization.py` | 213 |
| `ChannelwiseSplitPass` | Class | `ppq/quantization/optim/equalization.py` | 576 |
| `MatrixFactorizationPass` | Class | `ppq/quantization/optim/exprimental.py` | 183 |
| `ExtensionPass` | Class | `ppq/quantization/optim/extension.py` | 9 |
| `PPLCudaAddConvReluMerge` | Class | `ppq/quantization/optim/legacy.py` | 328 |
| `NXPResizeModeChangePass` | Class | `ppq/quantization/optim/morph.py` | 14 |
| `NCNNFormatGemmPass` | Class | `ppq/quantization/optim/morph.py` | 28 |
| `HorizontalLayerSplitPass` | Class | `ppq/quantization/optim/morph.py` | 51 |
| `MetaxGemmSplitPass` | Class | `ppq/quantization/optim/morph.py` | 201 |
| `GRUSplitPass` | Class | `ppq/quantization/optim/morph.py` | 218 |
| `PassiveParameterQuantizePass` | Class | `ppq/quantization/optim/parameters.py` | 12 |
| `ParameterQuantizePass` | Class | `ppq/quantization/optim/parameters.py` | 155 |
| `QuantizeSimplifyPass` | Class | `ppq/quantization/optim/refine.py` | 16 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Optimize → Get_upstream_operations` | cross_community | 6 |
| `Optimize → Get_downstream_operations` | cross_community | 6 |
| `Optimize → Add` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Finetune → Is_activated` | cross_community | 6 |
| `Correct_bias → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |
| `Optimize → Is_activated` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Algorithm | 6 calls |
| Analyse | 6 calls |
| IR | 3 calls |
| Executor | 2 calls |
| Qfunction | 1 calls |
| Observer | 1 calls |

## How to Explore

1. `gitnexus_context({name: "variable_analyse"})` — see callers and callees
2. `gitnexus_query({query: "optim"})` — find related execution flows
3. Read key files listed above for implementation details
