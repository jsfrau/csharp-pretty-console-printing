# PrettyConsolePrinting

A lightweight C# library for pretty console output of objects with type-based coloring and structured formatting.  
This repository includes the library and a demo console application.

## Projects

- `PrettyConsolePrinting/` — the library (intended for NuGet)
- `PrettyConsoleDemo/` — a console app with usage examples

## Features

- Extension methods:
    - `.ToCns()` — concise, human-friendly output
    - `.ToCnsExt()` — extended output (with indices for arrays, etc.)
- Type-aware colored output:
    - Integers → cyan
    - Floating point → magenta
    - Booleans → green/red
    - DateTime → blue
    - Strings/Chars/Enums → yellow (strings printed without quotes)
    - Null → gray
- Collections:
    - 1D arrays/lists: aligned elements
    - **2D arrays**: matrix-like formatting with aligned columns (default in `.ToCns()`)
    - Multidimensional arrays: recursive/extended formatting in `.ToCnsExt()`
- Dictionaries: ASCII tables with dynamic column widths
- Objects: public properties and fields via reflection  
  `ClassName { prop1: value1, prop2: value2 }`
- Nested collections supported
- Design patterns: Strategy, Singleton, polymorphism
- Performance: caching, lazy initialization, low allocations

## Getting Started

Build and run the demo:

```bash
dotnet build
dotnet run --project PrettyConsoleDemo
