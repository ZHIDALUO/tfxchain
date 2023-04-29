.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/TFXchain/tfx/cmd/swarm
	go build -o bin/geth     github.com/TFXchain/tfx/cmd/geth
	go build -o bin/bootnode github.com/TFXchain/tfx/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/TFXchain/tfx/swarm/...
