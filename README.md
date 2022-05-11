<p align = "center">
  <h3 align = "center"> Homarr <h3>

  <p align = "center">
    A homepage for <i>your</i> server.
  <br/>
  <a href = "https://github.com/ajnart/homarr/deployments/activity_log?environment=Production" > <strong> Demo ↗️ </strong> </a> • <a href = "#install" > <strong> Install ➡️ </strong> </a>
</p>
</p>

# 📃 Table of Contents
- [📃 Table of Contents](#-table-of-contents)
- [🚀 Getting Started](#-getting-started)
  - [ℹ️ About](#ℹ️-about)
  - [⚡ Installation](#-installation)
    - [Deploying from Docker Image 🐳](#deploying-from-docker-image-)
    - [Building from Source 🛠️](#building-from-source-️)

<!-- Getting Started -->
# 🚀 Getting Started

## ℹ️ About

Homarr is a simple and lightweight homepage for your server, that helps you easily access all of your services in one place.

## ⚡ Installation

### Deploying from Docker Image 🐳
> Supported architectures: x86-64, ARM, ARM64

_Requirements_:
- [Docker](https://docs.docker.com/get-docker/)

**Standard Docker Install**
```sh
docker run --name homarr -p 7575:80 -d ghcr.io/ajnart/mhp
```

**Docker Compose**
```yml
---
version: '3'
#--------------------------------------------------------------------------------------------#
#                               Homarr -  A homepage for your server.                        #
#--------------------------------------------------------------------------------------------#
services:
  mhp:
    container_name: homarr
    image: ghcr.io/ajnart/mhp
    restart: unless-stopped
    ports:
      - '7575:80'
```

### Building from Source 🛠️

_Requirements_:
- [Git](https://git-scm.com/downloads)
- [NodeJS](https://nodejs.org/en/) _(Latest or LTS)_
- [Yarn](https://yarnpkg.com/)
- Some web server

**Installing**

- Clone the GitHub repo: `git clone https://github.com/ajnart/homarr.git` & `cd myhomepage`
- Install all dependencies: `yarn install`
- Build the source: `yarn export`
- Start a web server (Any web server will work):
  - _Examples:_
    - NodeJS serve: `npm i -g serve` or `yarn global add serve` & `serve ./out`
    - python http.server: `python -m http.server 7474 --directory out`
