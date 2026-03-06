# lint-action

This will run:
* [`golangci-lint`](https://golangci-lint.run/)
    * [Config](./.golangci.yml)

**Overriding Go version and/or the golangci-lint version**

Using the inputs `go-version` and `golangci-lint-version` you can override the defaults.

For example, the below will use Go version 1.25.0 and golangci-lint version 2.5.0 in the repo where it's configured.

```
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: DefectDojo-Inc/lint-action@main
        with:
          go-version: '1.24.4'
          golangci-lint-version: 'v2.4.0'
```

