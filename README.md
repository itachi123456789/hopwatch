# Hopwatch, a debugging tool for Go

Hopwatch is an experimental tool in HTML5 that can help debugging Go programs. 
It works by communicating to a WebSockets based agent in Javascript.
When your program calls the Break function, it sends debug information to the browser page and waits for user interaction.
On the hopwatch page, the developer can view debug information and choose to proceed or terminate the execution of your program.

###Install
	go get github.com/emicklei/hopwatch

###Usage

	import (
		"github.com/emicklei/hopwatch"
	)
	
	func foo() {
		bar := "john"
		// stops execution until hitting "proceed" in the browser
		hopwatch.Display("foo", bar).Break()
	}

###Tool
Open the Hopwatch debugger on **http://localhost:23456/hopwatch.html** . Your browser must support HTML5 WebSockets.

To disable the breakpoints in your compiled program, pass the command line argument **-nobreak**

###Resources

- [project on github](https://github.com/emicklei/hopwatch)
- [blog](http://ernestmicklei.com)

(c) 2012, http://ernestmicklei.com. MIT License
	