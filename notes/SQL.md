# SQL

**Summary**: Notes on SQL and spatial-SQL engines — query optimization, spatial extensions, and geospatial database workflows.
**Last updated**: 2026-08-25

---

- [Optimizing DuckDB Spatial Queries](https://www.geomermaids.com/cookbook/duckdb-spatial/): Optimizing DuckDB Spatial Queries. Compares PostGIS and DuckDB spatial join approaches on identical FEMA flood data, showing that DuckDB's younger spatial extension needs explicit optimization PostGIS handles automatically — use `RTREE_INDEX_SCAN` only for constant-geometry predicates, avoid multiple spatial predicates per join, reproject to a metric CRS for `ST_DWithin`, and inline literal geometry values to enable Parquet row-group pruning. DuckDB, spatial SQL, PostGIS, RTREE index, Parquet, query optimization [[Remote_Sensing]]
