# Azure + Terraform

This repository contains the dockerfile to create an image with [Terraform](https://www.pulumi.com/),  [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest), [Powershell](https://github.com/PowerShell/PowerShell) and [SqlCmd](https://docs.microsoft.com/en-us/sql/tools/sqlcmd-utility?view=sql-server-ver15) installed

The main use for this is to ready-bake the installation.

Currently, this image is hosted on [Dockerhub](https://hub.docker.com/repository/docker/njlnick/az-terraform)

## Prerequisites

* [Docker](https://docs.docker.com/get-docker/)

## How to build image

```bash
docker build . --build-arg "TERRAFORM_VERSION=*terraform-version*"
```

e.g.

```bash
docker build . --build-arg "TERRAFORM_VERSION=1.0.4" -t zipnz/az-terraform:latest
docker build . --build-arg "TERRAFORM_VERSION=0.14.1" -t zipnz/az-terraform:0.14.1
docker build . --build-arg "TERRAFORM_VERSION=0.13.4" -t zipnz/az-terraform:0.13.4
...
```
