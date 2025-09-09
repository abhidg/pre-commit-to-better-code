# Pre-commit to better code

Accompanying repository for the RSECon25 walkthrough.

## Slides

Slides are written using dzslides, and are in a single standalone HTML file: [slides.html](slides.html)

## Walkthrough setup

Install [uv](https://github.com/astral-sh/uv) to be able to run the script with `uv run sunblock.py`. Alternatively you can create a virtual environment and install the dependencies:

```shell
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Also install [pre-commit](https://pre-commit.com/), installation instructions:

```shell
brew install pre-commit     # Homebrew
pip install pre-commit      # General, Windows
sudo apt install pre-commit # Debian/Ubuntu
sudo dnf install pre-commit # Fedora
```

## Language-specific hooks

- [Python](Python.md)

## Language-agnostic hooks

- [GitHub Actions](GitHubActions.md)

> [!NOTE]
> https://pre-commit.com/hooks.html has a good list of useful hooks
