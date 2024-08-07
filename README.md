# action-kcov

[![codecov](https://codecov.io/gh/sudo-bot/action-kcov/graph/badge.svg?token=NIDQPVEDWG)](https://codecov.io/gh/sudo-bot/action-kcov)

A GitHub action for kcov

## Example usage

```yml
name: Run tests

permissions:
  contents: read

on: [push]

jobs:
    test:
        name: Test the action
        runs-on: ubuntu-latest
        steps:
            - uses: actions/checkout@v4

            - name: Example with a bash script (running on Docker kcov/kcov:latest)
              uses: sudo-bot/action-kcov@latest
              with:
                cli-args: "--dump-summary ./coverage ./.github/workflows/test.sh"

            - name: Upload coverage reports to Codecov
              uses: codecov/codecov-action@v4
              with:
                # Must be set in the repo or org settings as a secret
                token: ${{ secrets.CODECOV_TOKEN }}
                directory: ./coverage/
                fail_ci_if_error: true
```
