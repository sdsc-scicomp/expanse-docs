# Expanse Supercomputer User Guide

Documentation for the Expanse supercomputer at the San Diego Supercomputer Center (SDSC).

**Published site:** <https://sdsc-scicomp.github.io/expanse-docs/>

## Contents

The documentation is written in Markdown and is organized into the following pages (see `docs/`):

- Technical Summary
- System Access
- Modules
- Account Management
- Job Charging
- Compiling Codes
- Running Jobs on Expanse
- Using GPU Nodes
- Expanse AI Resource
- Data Movement
- Storage
- Composable Systems
- Software
- Citations and Publications

## Source

This documentation is generated from the official [SDSC Expanse user guide](https://www.sdsc.edu/systems/expanse/user_guide.html). If the source guide is updated, update the corresponding pages under `docs/` and rebuild.

## Building the site

The site is built with [Zensical](https://zensical.org/), a static site generator created by the Material for MkDocs team. Zensical reads the existing `mkdocs.yml` configuration.

### Local development

```bash
# create a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# install dependencies
pip install -r requirements.txt

# serve with live reload
zensical serve

# build the static site into ./site
zensical build
```

### Publishing

The site is published to GitHub Pages at [https://sdsc-scicomp.github.io/expanse-docs/](https://sdsc-scicomp.github.io/expanse-docs/) using the workflow in `.github/workflows/docs.yml`, which builds with Zensical and deploys the `site/` output via GitHub Pages on every push to `main`.
