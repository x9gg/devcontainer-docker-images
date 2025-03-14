# Docker Images

## Base Image
`x9gg/image:base` - Debian bookworm-slim based development environment with git, curl, wget, vim, nano, zsh, network utilities.

## Node Images
- `x9gg/image:nodejs-20` - Node.js 20 LTS
- `x9gg/image:nodejs-22` - Node.js 22 Current

## Folder Structure
```
base/             # Base image
nodejs-20/        # Node.js 20 image
nodejs-22/        # Node.js 22 image
```

## Usage
```bash
# Build
cd base
docker build -t x9gg/image:base .

cd ../nodejs-20
docker build -t x9gg/image:nodejs-20 .

cd ../nodejs-22
docker build -t x9gg/image:nodejs-22 .

# Run
docker run -it --rm x9gg/image:nodejs-20
```

## Features
- ZSH shell with plugins
- Dev user (uid 1337) with sudo (`no password`)
- Common development tools