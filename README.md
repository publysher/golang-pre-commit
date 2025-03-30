# golang-pre-commit
Simple, opinionated pre-commit hooks for Go projects.

This will automatically run `go fmt`, `go test` and `go vet` on your commits. 

## Requirements

You need [Go](https://go.dev/) and [pre-commit](https://pre-commit.com/) installed on your system.
                             
## Usage

Add this repository to the `repos` in your `.pre-commit-config.yaml`: 

```yaml
repos:
  - repo: https://github.com/publysher/golang-pre-commit
    rev: v1.0.0
    hooks:
      - id: go-fmt
      - id: go-test
      - id: go-vet
```

Don't forget to run `pre-commit install` if you didn't use pre-commit before.

## Available hooks

* `go-fmt` runs `go fmt` on all changed Go files
* `go-test` runs your entire test suite using the `-short` flag. It will not fail if there are no tests.
* `go-vet` runs `go vet` on your entire project

## Configuration

There is no configuration. It's opinionated.  
