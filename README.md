# Golang Webview Example

This tiny app shows how to use the Go webview package at https://github.com/webview/webview. The package itself has very little documentation at https://pkg.go.dev/github.com/zserge/webview. It's basically just a wrapper around the various built-in browser renderers on Windows, Mac, and Linux.

This app demonstrates the following, with simple, well-commented code:

1. How to load a start page.
2. How to call Go code from JavaScript.
3. How to call JavaScript code from Go.

To run this, make sure you have Go 1.13 or higher. Clone this repo, cd into the top-level directory, then run `go run main.go`.

This has been tested on Mac OS Catalina, but should run on Windows and most flavors of Linux as well.

## Why?

We're evaluating webview as a possible alternative to Electron. In addition to being resource intensive, Electron requires we write everything in JavaScript, which means:

* a huge number of dependencies
* weekly dependency updates via Dependabot, often with breaking changes
* forced use of Node's async operations even when async is not appropriate

Our Electron app has about 2000 dependencies, while similar functionality in Go requires around 20 dependencies, most of which are more stable, better tested, and better documented.

For ease of getting started, Electron is a big win. For long-term maintenance, it's not. At all. In fact, it's a huge timesuck.

Webview's benefits:

* easy compile
* fewer and more stable dependencies
* smaller binary (<20 MB on Mac vs. Electron's 285 MB)
* less memory usage (<10 MB on startup, vs. Electron's 150 MB)
* more sane and stable ecosystem (Go vs. npm/yarn)
