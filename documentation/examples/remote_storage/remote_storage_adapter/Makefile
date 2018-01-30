ORGANIZATION=hyperpilot
IMAGE=remote_storage_adapter
TAG=latest

.PHONY: build docker-build docker-push

build:
	CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo
docker-build:
	docker build -t $(ORGANIZATION)/$(IMAGE):$(TAG) .
docker-push:
	docker push $(ORGANIZATION)/$(IMAGE):$(TAG)
