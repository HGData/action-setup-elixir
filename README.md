# action-setup-elixir

[![CI](https://github.com/HGData/action-setup-elixir/actions/workflows/main.yml/badge.svg)](https://github.com/HGData/action-setup-elixir/actions/workflows/main.yml)

## Overview

- Checks out the code
- Configures Elixir
- Fetches dependencies
- Manages build caching
## Usage

To utilize this composite action, use the following workflow syntax:
```yaml
- name: Setup Elixir
  uses: hgdata/action-setup-elixir
  with:
    elixir-version: ${{ matrix.pair.elixir }}
    otp-version: ${{ matrix.pair.otp }}
    with-oban: true
    oban-key-fingerprint: ${{ secrets.OBAN_KEY_FINGERPRINT }}
    oban-license-key: ${{ secrets.OBAN_LICENSE_KEY }}
    build-flags: --all-warnings --warnings-as-errors
```

Note that tags can be referenced with `@<tag>`.
