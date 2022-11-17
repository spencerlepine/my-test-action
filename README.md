# Typo scanner github action

Scans the given repo for typos

## Inputs

## `scan-exclude-match`

**Optional** List of file paths to ignore scanning for typos. Default `'[''typos/**'', ''public/**'']'`.


## Example usage

```yml
name: Test Action
on: push

jobs:
  test-action:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Run this action to test it
        uses: ./
        with:
          # Must use '' to properly escape the quotes
          scan-exclude-match: '[''typos/**'', ''public/**'']'
```