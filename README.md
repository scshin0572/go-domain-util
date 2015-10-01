# go-domain-tools

GOlang package for checking if url contains subdomain, what that subdomain is, what is a top level domain in url etc.

# Installation

`go get github.com/bobesa/go-domain-util/domainutil`

# Example code

```go
package main

import (
    "fmt"
)

import "github.com/bobesa/go-domain-util/domainutil"

func main(){
    fmt.Println(domainutil.Domain("keep.google.com"))
}
```

# Functions

## Get the top level domain from url
```go
func Domain(url string) string
```
Domain returns top level domain from url string. If no domain is found in provided url, this function returns empty string. If no TLD is found in provided url, this function returns empty string.

## Get the domain suffix from url
```go
func DomainSuffix(url string) string
```
DomainSuffix returns domain suffix from provided url. If no TLD is found in provided url, this function returns empty string.

## Check if url has subdomain
```go
func HasSubdomain(domain string) bool
```
HasSubdomain reports whether domain contains any subdomain.

## Get subdomain from url
```go
func Subdomain(url string) string
```
Subdomain returns subdomain from provided url. If subdomain is not found in provided url, this function returns empty string.