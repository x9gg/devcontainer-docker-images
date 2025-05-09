# Docker Images

## Base Image
`x9gg/image:base` - Debian bookworm-slim based development environment with git, curl, wget, vim, nano, zsh, network utilities.

## Node Images *LTS*
- `x9gg/image:nodejs-20` - Node.js 20 
- `x9gg/image:nodejs-22` - Node.js 22

## Go latest (1.24.1)
- `x9gg/image:go`        - go 1.24.1

## PHP latest (8.4.5 + composers 2.8.8)
- `x9gg/image:php-84`    - php 8.4 + composer 2.8.8

## Folder Structure
```
base/             # Base image
nodejs-20/        # Node.js 20 image
nodejs-22/        # Node.js 22 image
go/               # go 1.24.1 image
php-84/           # php 8.4 + composer
```

## Usage
```bash
# Build
cd base
docker build -t x9gg/image:base .

cd nodejs-20
docker build -t x9gg/image:nodejs-20 .

cd nodejs-22
docker build -t x9gg/image:nodejs-22 .

cd go
docker build -t x9gg/image:go .

cd php-84
docker build -t x9gg/image:php-84 .

# Run
docker run -it --rm x9gg/image:nodejs-20
```

## Features
- ZSH shell with plugins
- Dev user (uid 1337) with sudo (`no password`)
- Common development tools
