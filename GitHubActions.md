# GitHub Actions

The following pre-commit hook enables linting on GitHub Actions yaml files.

```yaml
  - repo: https://github.com/rhysd/actionlint
    rev: v1.7.7
    hooks:
      - id: actionlint
```
