# gotoolingcobra

this is the Linux Academy course System Tooling with Go

It implements a basic go application that asks for two items of input from the command line, lets you se what is required with a 'prompt' boolean and lets you see more details with a 'debug' bool.

it then writes this data to a file. In the original file it wrote the data to /etc/motd which meant altering several elements of the go path so i avoided that by writing to the current directory.

## Input Values

To prompt for the input values this version uses the cobra package not Go flags but is essentially the same application 

## cobra

cobra is a package for writing more complex and more manageable user cli inputs and ther is a version of this project from the same source at gotoolingcobra in my repos

## setting up cobra

please see the cobra site and the documentation for more details but here is my take on it

- run go get to install cobra on your machine
	- go get -u github.com/spf13/cobra/cobra
- then you run cobra
	- to do this you create a directory in the go/src directory (the whole $gopath thing from before modules) and run the cobra init command the final parameter '[USERNAME]/motd' is the directory you want the cobra code to be built in which can be outside of the $gopath (as it now should be) in a go mod environment
	- cobra init --pkg-name github.com/[USERNAME]/motd [USERNAME]/motd

after doing this then use the code in the cmd directory to craft the code.