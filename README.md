# Golang Webview Example

This tiny app shows how to use the Go webview package at https://github.com/webview/webview. The package itself has very little documentation at https://pkg.go.dev/github.com/zserge/webview. It's basically just a wrapper around the various built-in browser renderers on Windows, Mac, and Linux.

This app demonstrates the following, with simple, well-commented code:

1. How to load a start page.
2. How to call Go code from JavaScript.
3. How to call JavaScript code from Go.

To run this, make sure you have Go 1.13 or higher. Clone this repo, cd into the top-level directory, then run `go run main.go`.

This has been tested on Mac OS Catalina, but should run on Windows and most flavors of Linux as well.
