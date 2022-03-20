GO:=go
NAME:=coredns

clean:
	$(RM) -rf build && mkdir build

.PHONY: build
build: clean build-darwin build-windows build-linux-amd64 build-linux-arm64

build-darwin:
	GOOS=darwin GOARCH=amd64 $(GO) build -o build/coredns_darwin_amd64

build-windows:
	GOOS=windows GOARCH=amd64 $(GO) build -o build/coredns_windows_amd64.exe

build-linux-amd64:
	GOOS=linux GOARCH=amd64 $(GO) build -o build/coredns_linux_amd64

build-linux-arm64:
	GOOS=linux GOARCH=arm64 $(GO) build -o build/coredns_linux_arm64
