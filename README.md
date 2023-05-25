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
  uses: hgdata/action-setup-elixir@v1
  with:
    elixir-version: ${{ matrix.pair.elixir }}
    otp-version: ${{ matrix.pair.otp }}
    with-oban: true
    oban-key-fingerprint: ${{ secrets.OBAN_KEY_FINGERPRINT }}
    oban-license-key: ${{ secrets.OBAN_LICENSE_KEY }}
    build-flags: --all-warnings --warnings-as-errors
```

Note that there _must_ be a tag/branch reference.

## Releasing

To keep the changes minimal in repos that use this action we are adding a `v1` tag 
that must be manually pointed to the latest semver (e.g. v1.0.3) tag.

This allows users to do this `uses: hgdata/action-setup-elixir@v1` instead of `uses: hgdata/action-setup-elixir@v1.0.3`.
