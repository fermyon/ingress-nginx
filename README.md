# ingress-nginx Image Builder

A GitHub Action to build [ingress-nginx](https://github.com/kubernetes/ingress-nginx) container images from source using the [chainguard-forks/ingress-nginx](https://github.com/chainguard-forks/ingress-nginx) repository.

## What it does

This repository contains a manually-triggered GitHub Actions workflow that:

1. Clones [chainguard-forks/ingress-nginx](https://github.com/chainguard-forks/ingress-nginx) at a specified release tag
2. Compiles the ingress controller, debug tool, and pre-stop hook for both `amd64` and `arm64`
3. Builds a multi-platform Docker image and pushes it to `ghcr.io`

## Usage

1. Go to the **Actions** tab
2. Select the **Build ingress-nginx from source** workflow
3. Click **Run workflow**
4. Enter the release tag to build (e.g. `controller-v1.12.1`)
5. Click **Run workflow**

The resulting image will be published to:

```
ghcr.io/<owner>/ingress-nginx:<release-tag>
```
