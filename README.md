# Shopwell CLI GitHub Action

Easily install the [Shopwell CLI](https://github.com/shopwell-shop/shopwell-cli) in your GitHub Actions workflows. Ready-to-use for building and packaging Shopwell extensions in your CI pipelines.

## Prerequisites

- A GitHub repository using GitHub Actions.
- Recommended: Use on a Linux runner (e.g., `ubuntu-latest`).

## Setup

Create a file in your repository (e.g., `.github/workflows/shopwell-cli.yml`) with the following contents:

```yaml
name: shopwell-cli

on:
  pull_request:
  push:

permissions:
  contents: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
        with:
          fetch-depth: 0

      - name: Install Shopwell CLI
        uses: shopwell-shop/shopwell-cli-action@v3

      - name: Build and Package Extension
        run: shopwell-cli extension zip .
```

## More Information

For more Shopwell CLI documentation, visit [our developer docs](https://developer.shopwell.cn/docs/products/cli/).
