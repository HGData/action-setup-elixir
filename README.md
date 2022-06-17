# composite-action-template

Template repository for creating [GitHub composite actions](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action).
This text should be replaced with a short description of what the composite action does.

## Template instructions

***Don't manually create new repos from this template! Use Terraform instead.***

### Creating the templated repo

The preferred way to create a new repository is to add it to the Terraform configuration
in the [ops-github](https://github.com/HGData/ops-github) repo. This will ensure that when the repo is created,
it has the correct settings, permissions, branch protections, etc.

### Customizing the template

This template should work out of the box. Start by following the setup instructions below.

Some things you will want probably want to change:

1. This `README.md` file :)
1. Any stale content in `CHANGELOG.md`
1. `.github/dependabot.yml` to add the paths to any directories that need to be monitored
1. Customize the github actions status badge below

## Overview

Add a more in-depth overview of the new module here.

Customize the image/link below for the GHA workflow status.

[![CI](https://github.com/HGData/composite-action-template/actions/workflows/main.yml/badge.svg)](https://github.com/HGData/composite-action-template/actions/workflows/main.yml)

## Usage

To utilize this composite action, use the following workflow syntax:
```yaml
- name: Composite action
  uses: hgdata/composite-action-template@v1
```

Note that `uses` will accept typical tag references after the `@`.
