# Docker Images

## Base Image
`x9gg/image:base` - Debian bookworm-slim based development environment with git, curl, wget, vim, nano, zsh, network utilities.

## Node Images
- `x9gg/image:nodejs-20` - Node.js 20 LTS
- `x9gg/image:nodejs-22` - Node.js 22 Current

## Usage
```bash
# Build
docker build -t x9gg/image:base -f base.Dockerfile .
docker build -t x9gg/image:nodejs-20 -f node-20.Dockerfile .
docker build -t x9gg/image:nodejs-22 -f node-22.Dockerfile .

# Run
docker run -it --rm x9gg/image:nodejs-20
```

## Features
- ZSH shell with plugins
- Dev user (uid 1337) with sudo
- Common development tools