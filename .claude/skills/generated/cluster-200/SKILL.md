---
name: cluster-200
description: "Skill for the Cluster_200 area of ppq. 11 symbols across 1 files."
---

# Cluster_200

11 symbols | 1 files | Cohesion: 100%

## When to Use

- Working with code in `ppq/`
- Understanding how LogStreamConsumerBase, LogStreamConsumer, log work
- Modifying cluster_200-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `ppq/samples/TensorRT/lenet_demo/common/logging.h` | LogStreamConsumerBase, LogStreamConsumer, severityOstream, severityPrefix, log (+6) |

## Entry Points

Start here when exploring this area:

- **`LogStreamConsumerBase`** (Class) — `ppq/samples/TensorRT/lenet_demo/common/logging.h:110`
- **`LogStreamConsumer`** (Class) — `ppq/samples/TensorRT/lenet_demo/common/logging.h:131`
- **`log`** (Method) — `ppq/samples/TensorRT/lenet_demo/common/logging.h:243`
- **`getReportableSeverity`** (Method) — `ppq/samples/TensorRT/lenet_demo/common/logging.h:371`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `LogStreamConsumerBase` | Class | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 110 |
| `LogStreamConsumer` | Class | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 131 |
| `log` | Method | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 243 |
| `getReportableSeverity` | Method | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 371 |
| `LOG_VERBOSE` | Function | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 455 |
| `LOG_INFO` | Function | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 467 |
| `LOG_WARN` | Function | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 479 |
| `LOG_ERROR` | Function | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 491 |
| `LOG_FATAL` | Function | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 504 |
| `severityOstream` | Method | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 159 |
| `severityPrefix` | Method | `ppq/samples/TensorRT/lenet_demo/common/logging.h` | 164 |

## How to Explore

1. `gitnexus_context({name: "LogStreamConsumerBase"})` — see callers and callees
2. `gitnexus_query({query: "cluster_200"})` — find related execution flows
3. Read key files listed above for implementation details
