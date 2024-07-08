# action-kcov

A GitHub action for kcov

## Example usage

```yml
    - uses: actions/checkout@v4
    - name: get kcov version
        uses: sudo-bot/action-kcov@latest
        with:
            cli-args: "--version"
```
