[![This project is considered stable](https://img.shields.io/badge/Status-stable-green.svg)](https://arp242.net/status/stable)
[![Build Status](https://travis-ci.org/arp242/goimport.svg?branch=master)](https://travis-ci.org/arp242/goimport)
[![codecov](https://codecov.io/gh/arp242/goimport/branch/master/graph/badge.svg)](https://codecov.io/gh/arp242/goimport)

`goimport` is a tool to add, remove, or replace imports in Go files.

Install it with `go get arp242.net/goimport`.

Example usage:

```shell
# Add errors package.
$ goimport -add errors foo.go

# Remove errors package.
$ goimport -rm errors foo.go

# Add errors package aliased as "errs"
$ goimport -add errors:errs foo.go

# Either add an import or replace existing errors with
# github.com/pkg/errors.
$ goimport -replace github.com/pkg/errors foo.go

# Try to "go get" package if it's not found.
$ goimport -get -add github.com/pkg/errors foo.go

# Print out only the import block as JSON (useful for editor integrations).
$ goimport -json -add github.com/pkg/errors foo.go
```

See `goimport -h` for the full help.
