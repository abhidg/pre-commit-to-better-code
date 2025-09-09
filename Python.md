# Python pre-commit configs

It is always recommended to enable the base config that pre-commit provides (`pre-commit sample-config`). These snippets are in addition to the base config.

## Linting

```yaml
- repo: https://github.com/astral-sh/ruff-pre-commit
  # Ruff version.
  rev: v0.12.12
  hooks:
    # Run the linter.
    - id: ruff-check
      args: [ --fix ]
```

## Autoformatting

```yaml
- repo: https://github.com/astral-sh/ruff-pre-commit
  rev: v0.12.12
  hooks:
    # Run the formatter.
    - id: ruff-format
```

Hooks under the same repo can also be combined:

```yaml
- repo: https://github.com/astral-sh/ruff-pre-commit
  # Ruff version.
  rev: v0.12.12
  hooks:
    # Run the linter.
    - id: ruff-check
      args: [ --fix ]
    # Run the formatter.
    - id: ruff-format
```

## Typechecking

```yaml
-   repo: https://github.com/pre-commit/mirrors-mypy
    rev: v1.17.1  # Use the sha / tag you want to point at
    hooks:
      - id: mypy
        # next line is optional, if you want to install type stubs
        # additional_dependencies: [types-requests]
```

## Finding undeclared dependencies

[FawltyDeps](https://tweag.github.io/FawltyDeps) finds missing or undeclared dependencies as well as unused dependencies. It can be run in CI and as a pre-commit hook.

```yaml
- repo: https://github.com/tweag/FawltyDeps
  rev: v0.20.0
  hooks:
     - id: check-undeclared
     - id: check-unused
```
