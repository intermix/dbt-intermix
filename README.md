This [dbt](https://github.com/fishtown-analytics/dbt) package contains macros that are useful for [Intermix](https://intermix.io/) users.

## Installation Instructions
Check [dbt Hub](https://hub.getdbt.com/intermix/dbt-intermix/latest/) for the latest installation instructions, or [read the docs](https://docs.getdbt.com/docs/package-management) for more information on installing packages.

----

## Macros
### track ([source](macros/query_header.sql))
This macro returns JSON-formatted informaton about a running dbt node (a model, test, etc). This macro can
be used to inject a comment into the header of the queries that dbt generates and runs.

Usage:
```
# dbt_project.yml

query-comment: "{{ intermix.track(node) }}"
```
