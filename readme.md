# GO Lang for VS Code (Intro)
## Repo at - https://github.com/jtc10005/GoLang-Start

### steps for go lang
1. download the go compiler from https://golang.org/dl/
2. Install and set up go:
	a. verify that go is in path env var (https://golang.org/doc/install?download=go1.10.windows-amd64.msi)
	b. test go from command line
		1. open command prompt and type go version.  Should see go version info

For vscode, install 
add the go extension:
https://code.visualstudio.com/docs/languages/go

install delve (https://github.com/derekparker/delve)
run the following from the command line: 
go get -u github.com/derekparker/delve/cmd/dlv

then, still from command line, install gopkgs
go get -v github.com/uudashr/gopkgs/cmd/gopkgs

open vscode and navigate to %USERPROFILE%\go
this is the default path for go.  If you want to dev somewhere else you need to set the go path.  see instructions from here: https://github.com/golang/go/wiki/SettingGOPATH

create a folder called test.
from https://www.tutorialspoint.com/go/go_program_structure.htm
In this folder create a file called main.go and paste the following into the file.

	package main

	import "fmt"

	func main() {
	    fmt.Printf("hello, world\n")
	}

hit f5 to debug (need to setup launch.json for go)
console should display "hello world".