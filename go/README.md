# Unchained (Go)

## Project Structure

- `pkg` - shared common packages across coinstacks
- `internal` - internal utility packages
- `coinstacks/{coin}` - coin specific logic

## Dependencies

- [go](https://go.dev/)
- [goimports](https://pkg.go.dev/golang.org/x/tools/cmd/goimports)
- [golangci-lint](https://golangci-lint.run/)

## Notes

- It is suggested configuring your editor of choice to utilize the following tooling:
  - [gopls](https://pkg.go.dev/golang.org/x/tools/gopls) language server
  - [golangci-lint](https://golangci-lint.run/) to match the linter used in CI
  - [goimports](https://pkg.go.dev/golang.org/x/tools/cmd/goimports) to match the formatting run on git pre-commit hook (default behavior when using gopls)
- Visual Studio Code expects any golang projects to be opened up with a `go.mod` file at the root directory for the tooling to work properly, so be sure to open up the project at `unchained/go`

## Initial Setup

- Any commands should be run from within `unchained/go`

- Install [Golang](https://go.dev/doc/install)

- Make coinstacks

  ```sh
  make
  ```

- Copy sample env file:

  ```sh
  cp cmd/ethereum/sample.env cmd/ethereum/.env
  ```

- Fill out any missing variables
  - Create a [Datahub Account](https://datahub-beta.figment.io/signup) for a free API key