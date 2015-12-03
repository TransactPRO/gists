# OSX/Linux

[Download archive](https://storage.googleapis.com/golang/go1.5.1.darwin-amd64.tar.gz) (64-bit)

Open terminal enter `Downloads` folder and unpack it `/usr/local`.

```bash
$ cd Downloads

$ tar -C /usr/local -xzf go1.5.1.darwin-amd64.tar.gz
```
Now, create `.profile` file and add `go` to path by executing:

```bash
$ cd

$ echo 'export PATH=$PATH:/usr/local/go/bin' > .profile

$ source .profile
```

Check, that it is working by executing `go` command in terminal. You shold see help of go tool.

Create our working directory and project folder:

```bash
$ mkdir -p workspace/we-are-ready
```

Let's set our workspace to `GOPATH` variable:

```bash
$ echo 'export GOPATH=$HOME/workshop' >> .profile

$ source .profile

$ cd workshop/we-are-ready

$ nano first.go
```

We created file `first.go` in our project directory, copy & paste following code in there:

```go
package main

import "fmt"

func main() {
    fmt.Printf("We are ready!!!")
}
```

Save it and execute our first application:

```bash
$ go run first.go
We are ready!
```

# Windows

[Downolad MSI installer](https://storage.googleapis.com/golang/go1.5.1.windows-amd64.msi) (64-bit)

Open it and make installation. It will install everything for you.

Now go to `Controll Panel > Settings > Advanced Settings` and open `Environment Variables`

Add new variable `GOPATH` with value `%USERPROFILE%/work`

`work` is a folder in your user home directory.

Create in `work` directory new directory named `we-are-ready`.

Create there file `example.go`

And copy & paste there:

```go
package main

import "fmt"

func main() {
    fmt.Printf("We are ready!\n")
}
```

(Path were we are is `work/we-are-ready/example.go`)

Open terminal, type:

```shell
C:\Users\tpro> cd work/we-are-ready

C:\User\tpro\work\we-are-ready> go run example.go
We are ready!
```
