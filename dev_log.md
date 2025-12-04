# Development Log – Charvi

## 2025-11-28
- Set up the folder for my part of the project.
- Added the main files I would be working on: registry.py, inspector.py, codegen.py, run_tests.py, run_benchmarks.py, and this dev_log.
- My goal was to create small Jai-style debugging features in Python so we could compare ideas from the talk.

## 2025-11-29
- Started working on the registry system.
- Implemented FastRegistry using a dictionary (expected O(1) lookup).
- Also added SlowRegistry using a list so I could compare the two and show the difference in performance.
- Wrote a small test in run_tests.py to make sure registration and lookups were working properly.

## 2025-11-30
- Continued with the inspector tool.
- Added DFS-based object inspection that collects information about objects and their attributes.
- Added simple cycle detection and a depth limit so the inspector wouldn’t get stuck.
- Cleaned up some edge cases and printed a few inspection outputs for testing.

## 2025-12-01
- Worked on codegen.py.
- Added template expansion and a basic caching mechanism so repeated calls are faster.
- Connected everything so the registry, inspector and codegen parts work independently.

## 2025-12-02
- Ran benchmark tests for FastRegistry vs SlowRegistry.
- Used run_benchmarks.py to collect simple timing results.

### Registry Lookup Times  
Format: n, FastRegistry (s), SlowRegistry (s)

100, 0.00000021, 0.00000112
1000, 0.00000038, 0.00001017
5000, 0.00000079, 0.00004271

