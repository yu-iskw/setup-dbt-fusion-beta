# setup-dbt-fusion-beta

This is a GitHub Action to setup [dbt Fusion](https://www.getdbt.com/product/fusion) in beta.

**NOTE:**
I suppose the way to install dbt Fusion isn't finalized yet as of July 2025.
I don't guarantee the dedicated support for the action.
I plan to create a new action or rename this action to `setup-dbt-fusion` when the way to install dbt Fusion is finalized.

## Usage

```yaml
jobs:
  dbt-build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Setup dbt Fusion
        uses: ${{ github.repository }}@v1
        with:
          dbt-version: 1.7.1
```
