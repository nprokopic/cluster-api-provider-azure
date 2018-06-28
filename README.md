# k8s Cluster API Azure Provider [![Build Status](https://travis-ci.org/platform9/azure-provider.svg?branch=master)](https://travis-ci.org/platform9/azure-provider) [![Go Report Card](https://goreportcard.com/badge/github.com/platform9/azure-provider)](https://goreportcard.com/report/github.com/platform9/azure-provider)

## Notes
cluster-api should be vendored when testing, either in Travis or locally, but should not be versioned in git. This allows the cluster-api to import `azure-provider` while avoiding a circular dependency. To vendor the cluster-api for testing purposes, un-ignore it in `Gopkg.toml` and run `dep ensure -add sigs.k8s.io/cluster-api/pkg -vendor-only`. After adding it, `Gopkg.lock` will reference it. Prior to comitting, this should be manually removed.