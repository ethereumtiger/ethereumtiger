.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/ethereumtiger/ethereumtiger/cmd/swarm
	go build -o bin/geth     github.com/ethereumtiger/ethereumtiger/cmd/geth
	go build -o bin/bootnode github.com/ethereumtiger/ethereumtiger/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/ethereumtiger/ethereumtiger/swarm/...
