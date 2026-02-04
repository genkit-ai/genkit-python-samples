# How to contribute to Genkit Python Samples

We'd love to accept your patches and contributions to this project.

## Before you begin

### Sign our Contributor License Agreement

Contributions to this project must be accompanied by a
[Contributor License Agreement](https://cla.developers.google.com/about) (CLA).
You (or your employer) retain the copyright to your contribution; this simply
gives us permission to use and redistribute your contributions as part of the
project.

If you or your current employer have already signed the Google CLA (even if it
was for a different project), you probably don't need to do it again.

Visit <https://cla.developers.google.com/> to see your current agreements or to
sign a new one.

### Review our community guidelines

This project follows
[Google's Open Source Community Guidelines](https://opensource.google/conduct/).

## Contribution process

### Code reviews

All submissions, including submissions by project members, require review. We
use GitHub pull requests for this purpose. Consult
[GitHub Help](https://help.github.com/articles/about-pull-requests/) for more
information on using pull requests.

## Setup

This repository uses [uv](https://github.com/astral-sh/uv) for Python dependency management and [pnpm](https://pnpm.io/) for some web assets/tooling.

1.  **Install `uv`**:
    Follow the [official installation guide](https://github.com/astral-sh/uv?tab=readme-ov-file#installation).

2.  **Install `pnpm`** (if working on web samples that require it):
    Follow the [official installation guide](https://pnpm.io/installation).

3.  **Sync dependencies**:
    ```bash
    uv sync
    pnpm install
    ```

## Development Workflow

### Adding a new sample app

1.  Create a new directory in `apps/`.
2.  Add a `pyproject.toml` and `README.md`.
3.  Add a `run.sh` script.
4.  Add your app logic.
5.  Add it to the workspace in root `pyproject.toml` (under `[tool.uv.sources]`).

### Linting and Formatting

Before submitting a PR, ensure your code is linted and formatted correctly.

**Format (Auto-fix)**:
```bash
bin/fmt
```

**Lint (Check)**:
```bash
bin/lint
```

### Running Tests

Run tests using pytest via uv:

```bash
uv run pytest
```
