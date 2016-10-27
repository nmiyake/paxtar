paxtar
------
`paxtar` is a copy of Go's `archive/tar` package from Go 1.7.3. The only difference is the addition of the
`NewPaxWriter` function to `writer.go`. This function can be used to create a Writer that always prefers using PAX
headers. Although the PAX standard is slightly less compatible (defined in 2001), it is still widely used, and always
using PAX headers resolves issues such as https://github.com/golang/go/issues/17630.
