# action-kcov

A GitHub action for kcov

## Example usage

```yml
    - uses: actions/checkout@v2
    - name: get kcov version
        uses: sudo-bot/action-kcov
        with:
            cli-args: "--version"
```
