.PHONY: build
build:
	go build -o bin/myclient client.go

.PHONY: run
run:
	./bin/myclient localhost:9091 | jq .

.PHONY: run-testprog-with-dlv
run-testprog-with-dlv:
	cd ./testprog && dlv debug --headless --api-version=2 --accept-multiclient --listen :9091

.PHONY: kill-dlv-server
kill-dlv-server:
	pkill dlv