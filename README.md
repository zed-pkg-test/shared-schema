# shared-schema

One language-neutral JSON Schema shared by several repositories.

The repository intentionally supports two independent consumption paths:

1. **Git vendoring** for `submodule-consumer` and `subtree-consumer`, which test how `zed publish` treats content already present through Git mechanisms.
2. **Zed package installation** as `zedtest/shared-schema@1.0.0`, used by heterogeneous Node, Go, and Python consumer projects.

Neither path replaces the other. The source bytes are identical, which lets CI compare Git-vendored and registry-installed provenance without maintaining duplicate schema repositories.

## Contract

`schemas/job-envelope.schema.json` defines a small cross-language job envelope with `greet` and `slugify` operations.

## License

MIT
