FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

# Install Node.js (example using Node 22 LTS) + Python 3.10 + build tools
RUN apt-get update && \
    apt-get install -y curl software-properties-common build-essential cmake git && \
    # Add deadsnakes PPA for older Python versions
    add-apt-repository ppa:deadsnakes/ppa -y && \
    apt-get update && \
    apt-get install -y \
        python3.10 \
        python3.10-dev \
        python3.10-distutils \
        python3.10-venv \
        python3-pip \
        python-is-python3 && \
    curl -fsSL https://deb.nodesource.com/setup_22.x | bash - && \
    apt-get install -y nodejs && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Make Python 3.10 the default
RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 1 \
 && update-alternatives --install /usr/bin/python python /usr/bin/python3.10 1


