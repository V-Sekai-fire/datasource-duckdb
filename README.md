# datasource-duckdb

Lean 4 bindings to DuckDB for reading Parquet, CSV and JSON files into Lean.

## What it is for

A data source that loads dataset files into the same language that states the properties they must satisfy. The binding is a small C shim over DuckDB's C interface, linked statically against a DuckDB archive the package builds from source on its first build.

## Build and run

The build needs Linux with glibc: it links with GNU ld group flags and a glibc compatibility shim.

    lake build
    lake exe duckdb-demo

With no arguments the demo round-trips a small table through Parquet as a self-test.

A package that requires this one adds the same `moreLinkArgs` that `lakefile.lean` sets.

## Licence

MIT. See [LICENSE](LICENSE).
