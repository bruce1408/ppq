---
name: scheduler
description: "Skill for the Scheduler area of ppq. 23 symbols across 4 files."
---

# Scheduler

23 symbols | 4 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how value_tracing_pattern, SOI_receivers, SOI_generators work
- Modifying scheduler-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/scheduler/dispatchers.py` | AggresiveDispatcher, ConservativeDispatcher, PPLNNDispatcher, PointDispatcher, dispatch (+5) |
| `ppq/scheduler/perseus.py` | Perseus, solve_transitive_closure, mark_quantable_op, mark_soi_op, parse_transitive_fanout (+3) |
| `ppq/scheduler/base.py` | GraphDispatcher, value_tracing_pattern, SOI_receivers, SOI_generators |
| `ppq/scheduler/allin.py` | AllinDispatcher |

## Entry Points

Start here when exploring this area:

- **`value_tracing_pattern`** (Function) — `ppq/scheduler/base.py:25`
- **`SOI_receivers`** (Function) — `ppq/scheduler/base.py:59`
- **`SOI_generators`** (Function) — `ppq/scheduler/base.py:69`
- **`AllinDispatcher`** (Class) — `ppq/scheduler/allin.py:7`
- **`GraphDispatcher`** (Class) — `ppq/scheduler/base.py:5`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `AllinDispatcher` | Class | `ppq/scheduler/allin.py` | 7 |
| `GraphDispatcher` | Class | `ppq/scheduler/base.py` | 5 |
| `AggresiveDispatcher` | Class | `ppq/scheduler/dispatchers.py` | 16 |
| `ConservativeDispatcher` | Class | `ppq/scheduler/dispatchers.py` | 136 |
| `PPLNNDispatcher` | Class | `ppq/scheduler/dispatchers.py` | 277 |
| `PointDispatcher` | Class | `ppq/scheduler/dispatchers.py` | 417 |
| `Perseus` | Class | `ppq/scheduler/perseus.py` | 8 |
| `value_tracing_pattern` | Function | `ppq/scheduler/base.py` | 25 |
| `SOI_receivers` | Function | `ppq/scheduler/base.py` | 59 |
| `SOI_generators` | Function | `ppq/scheduler/base.py` | 69 |
| `dispatch` | Method | `ppq/scheduler/dispatchers.py` | 36 |
| `dispatch` | Method | `ppq/scheduler/dispatchers.py` | 159 |
| `dispatch` | Method | `ppq/scheduler/dispatchers.py` | 300 |
| `dispatch` | Method | `ppq/scheduler/dispatchers.py` | 439 |
| `solve_transitive_closure` | Method | `ppq/scheduler/perseus.py` | 75 |
| `mark_quantable_op` | Method | `ppq/scheduler/perseus.py` | 125 |
| `mark_soi_op` | Method | `ppq/scheduler/perseus.py` | 130 |
| `parse_transitive_fanout` | Method | `ppq/scheduler/perseus.py` | 155 |
| `parse_transitive_fanin` | Method | `ppq/scheduler/perseus.py` | 171 |
| `dispatch` | Method | `ppq/scheduler/perseus.py` | 187 |

## How to Explore

1. `gitnexus_context({name: "value_tracing_pattern"})` — see callers and callees
2. `gitnexus_query({query: "scheduler"})` — find related execution flows
3. Read key files listed above for implementation details
