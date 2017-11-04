[![This project is considered stable](https://img.shields.io/badge/Status-stable-green.svg)](https://arp242.net/status/stable)
[![GoDoc](https://godoc.org/arp242.net/goimport?status.svg)](https://godoc.org/arp242.net/goimport)
[![Go Report Card](https://goreportcard.com/badge/github.com/Carpetsmoker/goimport)](https://goreportcard.com/report/github.com/Carpetsmoker/goimport)
[![Build Status](https://travis-ci.org/Carpetsmoker/goimport.svg?branch=master)](https://travis-ci.org/Carpetsmoker/goimport)
[![codecov](https://codecov.io/gh/Carpetsmoker/goimport/branch/master/graph/badge.svg)](https://codecov.io/gh/Carpetsmoker/goimport)

`goimport` is a tool to add, remove, or replace imports in Go files.

Example usage:

	# Add errors package.
	$ goimport -add errors foo.go

	# Remove errors package.
	$ goimport -rm errors foo.go

	# Add errors package aliased as "errs"
	$ goimport -add errors:errs foo.go

	# Either add an import or replace existing errors with
	# github.com/pkg/errors.
	$ goimport -replace github.com/pkg/errors foo.go

	# Go get package if it doesn't exist
	$ goimport -add github.com/pkg/errors -g foo.go

	# Print out only the import block & everything before it (useful for
	# editor integrations).
	$ goimport -add github.com/pkg/errors -b foo.go

See `goimport -h` for the full help.

TODO:

- Make `-rm` deal with named imports.
