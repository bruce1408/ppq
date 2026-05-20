---
name: qat
description: "Skill for the Qat area of ppq. 8 symbols across 1 files."
---

# Qat

8 symbols | 1 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how QuantLayer, QConv1d, QConv2d work
- Modifying qat-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/qat/core.py` | QuantLayer, QConv1d, QConv2d, QConv3d, __init__ (+3) |

## Entry Points

Start here when exploring this area:

- **`QuantLayer`** (Class) — `ppq/qat/core.py:13`
- **`QConv1d`** (Class) — `ppq/qat/core.py:23`
- **`QConv2d`** (Class) — `ppq/qat/core.py:46`
- **`QConv3d`** (Class) — `ppq/qat/core.py:69`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `QuantLayer` | Class | `ppq/qat/core.py` | 13 |
| `QConv1d` | Class | `ppq/qat/core.py` | 23 |
| `QConv2d` | Class | `ppq/qat/core.py` | 46 |
| `QConv3d` | Class | `ppq/qat/core.py` | 69 |
| `__init__` | Method | `ppq/qat/core.py` | 14 |
| `__init__` | Method | `ppq/qat/core.py` | 24 |
| `__init__` | Method | `ppq/qat/core.py` | 47 |
| `__init__` | Method | `ppq/qat/core.py` | 70 |

## How to Explore

1. `gitnexus_context({name: "QuantLayer"})` — see callers and callees
2. `gitnexus_query({query: "qat"})` — find related execution flows
3. Read key files listed above for implementation details
