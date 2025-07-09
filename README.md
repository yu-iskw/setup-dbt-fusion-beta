# setup-dbt-fusion-beta

This is a GitHub Action to setup [dbt Fusion](https://www.getdbt.com/product/fusion) in beta.

dbt Fusion is an upcoming dbt Labs product that enables users to manage dbt projects and run dbt commands in a serverless environment. This action simplifies the setup of dbt Fusion within your GitHub Actions workflows, allowing you to easily integrate dbt Fusion into your CI/CD pipelines.

**NOTE:**
I suppose the way to install dbt Fusion isn't finalized yet as of July 2025.
I don't guarantee the dedicated support for the action.
I plan to create a new action or rename this action to `setup-dbt-fusion` when the way to install dbt Fusion is finalized.

## Usage

To use this action, add the following step to your GitHub Actions workflow:

```yaml
jobs:
  dbt-build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: yu-iskw/setup-dbt-fusion-beta@v1.0.0
```

### Inputs

- `dbt-version`: (Required) The version of dbt Fusion (or a dbt package like `dbt-core`) to install. This corresponds to the `--version` flag in the dbt Fusion installer.
- `package`: (Optional) The specific dbt package to install (e.g., `dbt`, `dbt-lsp`). If not specified, the installer will determine the default package. This corresponds to the `--package` flag in the dbt Fusion installer.
- `target`: (Optional) The target platform for the dbt Fusion installation (e.g., `x86_64-unknown-linux-gnu`, `aarch64-apple-darwin`). If not specified, the platform will be auto-detected. This corresponds to the `--target` flag in the dbt Fusion installer.
