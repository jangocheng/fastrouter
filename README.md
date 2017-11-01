# FastRouter

FastRouter is a fast, flexible HTTP router written in Go.

FastRouter exports options to custom router, such as `TrailingSlashesPolicy`, `PanicHandler`, `OptionsHandler`,
 `MethodNotAllowedHandler`, `NotFoundHandler` and so on.

FastRouter also provides some useful features, such as **grouping** and **middleware**.

[![GoDoc](https://godoc.org/github.com/razonyang/fastrouter?status.svg)](https://godoc.org/github.com/razonyang/fastrouter)
[![Build Status](https://travis-ci.org/razonyang/fastrouter.svg?branch=master)](https://travis-ci.org/razonyang/fastrouter)
[![Go Report Card](https://goreportcard.com/badge/github.com/razonyang/fastrouter)](https://goreportcard.com/report/github.com/razonyang/fastrouter)
[![Coverage Status](https://coveralls.io/repos/github/razonyang/fastrouter/badge.svg?branch=master)](https://coveralls.io/github/razonyang/fastrouter?branch=master)

# Features

**Fast**: See [Benchmark](#benchamrk)

**Flexible**: FastRouter export some useful options for you:
- TrailingSlashesPolicy: there are four policies available:
    - IgnoreTrailingSlashes: ignore trailing slashes.
    - AppendTrailingSlashes: append trailing slashes and redirect if request path is not end with '/'.
    - RemoveTrailingSlashes: remove trailing slashes and redirect if request path is end with '/'.
    - StrictTrailingSlashes: remove or append trailing slashes according to corresponding pattern.
- PanicHandler
- OptionsHandler
- MethodNotAllowedHandler
- NotFoundHandler

**Compatible**: FastRouter is an implementation of http.Handler, so it is compatible with third-party packages.

**Middleware**: Middleware is a chaining tool for chaining `http.Handler`,
 see [Middleware example](https://godoc.org/github.com/razonyang/fastrouter#example_Middleware).

**Grouping**: Grouping is an useful feature of FastRouter, it allows to nest and specify middleware of group,
 see [Grouping example](https://godoc.org/github.com/razonyang/fastrouter#example_Router_Group).


# Documentation

See [Documentation](https://godoc.org/github.com/razonyang/fastrouter)
 for details.

# Examples

- [Basic example](https://godoc.org/github.com/razonyang/fastrouter#example_)
- [Grouping example](https://godoc.org/github.com/razonyang/fastrouter#example_Router_Group)
- [Middleware example](https://godoc.org/github.com/razonyang/fastrouter#example_Middleware)
- [Serve static files example](https://godoc.org/github.com/razonyang/fastrouter#example_Router_ServeFiles)

See [Examples](https://godoc.org/github.com/razonyang/fastrouter#pkg-examples) for details.

# Benchmark

![Benchmark](https://github.com/razonyang/go-web-framework-benchmark/raw/master/benchmark.png)