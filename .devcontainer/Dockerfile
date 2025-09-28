FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

# Install Node.js (example using Node 22 LTS) + Python + build tools
RUN apt-get update && \
    apt-get install -y curl python3 python3-pip python-is-python3 build-essential cmake git && \
    curl -fsSL https://deb.nodesource.com/setup_22.x | bash - && \
    apt-get install -y nodejs && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

