# drone-k8s-deployment

[![Build Status](https://drone.pelo.tech/api/badges/josmo/drone-k8s-deployment/status.svg)](https://drone.pelo.tech/josmo/drone-k8s-deployment)
[![Go Doc](https://godoc.org/github.com/josmo/drone-k8s-deployment?status.svg)](http://godoc.org/github.com/josmo/drone-k8s-deployment)
[![Go Report](https://goreportcard.com/badge/github.com/josmo/drone-k8s-deployment)](https://goreportcard.com/report/github.com/josmo/drone-k8s-deployment)
[![](https://images.microbadger.com/badges/image/peloton/drone-k8s-deployment.svg)](https://microbadger.com/images/peloton/drone-k8s-deployment "Get your own image badge on microbadger.com")

Drone plugin to update a deployment in k8s. For the usage information and a listing of the available options please take a look at [the docs](DOCS.md).

## Binary

Build the binary using `go build`:


### Example

## Usage

Build and deploy from your current working directory:

```
docker run --rm                          \
  -e PLUGIN_URL=<source>                 \
  -e PLUGIN_TOKEN=<token>                \
  -e PLUGIN_CERT=<cert>                  \
  -e PLUGIN_INSECURE=<true>              \
  -e PLUGIN_DEPLOYMENT_NAME=<deployment> \
  -e PLUGIN_CONTAINER_NAME=<container>   \
  -e PLUGIN_NAMESPACE=<namespace>        \ 
  -e PLUGIN_DOCKER_IMAGE=<image>         \
  -v $(pwd):$(pwd)                       \
  -w $(pwd)                              \
  peloton/drone-k8s-deployment 
```