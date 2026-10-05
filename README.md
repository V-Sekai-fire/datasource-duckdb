# datasource-duckdb

Lean 4 bindings to DuckDB for reading Parquet, CSV and JSON files into Lean.

## What it is for

A data source that loads dataset files into the same language that states the properties they must satisfy. The binding is a small C shim over DuckDB's C interface, linked statically against a DuckDB archive the package builds from source on its first build.

## Build and run

    lake build
    lake exe duckdb-demo

With no arguments the demo round-trips a small table through Parquet as a self-test.

## Licence

MIT. See [LICENSE](LICENSE).
