Example of checksum error for envoy

```shell
go clean -modcache
go mod tidy
```
Result:
```
go: finding module for package github.com/envoyproxy/go-control-plane/envoy
go: downloading github.com/envoyproxy/go-control-plane/envoy v1.32.3
go: github.com/emilhauk/envoy-checksum-error imports
	github.com/envoyproxy/go-control-plane/envoy: github.com/envoyproxy/go-control-plane/envoy@v1.32.3: verifying module: checksum mismatch
	downloaded: h1:c1EIw4vwYCaovxRZtyycws8aX6dJ9W2p+4bCi7mcDgw=
	sum.golang.org: h1:hVEaommgvzTjTd4xCaFd+kEQ2iYBtGxP6luyLrx6uOk=

SECURITY ERROR
This download does NOT match the one reported by the checksum server.
The bits may have been replaced on the origin server, or an attacker may
have intercepted the download attempt.

For more information, see 'go help module-auth'.```

