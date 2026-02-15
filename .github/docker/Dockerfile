FROM ubuntu:22.04

# Avoid interactive prompts during build
ENV DEBIAN_FRONTEND=noninteractive

# Update and install minimalist set of required libraries
RUN apt-get update && apt-get install -y \
    build-essential \
    bash \
    bc \
    binutils \
    bison \
    bzip2 \
    curl \
    file \
    flex \
    g++ \
    gawk \
    gcc \
    gettext \
    git \
    libncurses5-dev \
    libpcre3-dev \
    libssl-dev \
    make \
    perl \
    python3 \
    python3-cryptography \
    python3-pyelftools \
    python3-dev \
    python3-distutils \
    python3-setuptools \
    quilt \
    rsync \
    sed \
    subversion \
    sudo \
    swig \
    tar \
    unzip \
    wget \
    zlib1g-dev \
    zstd \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Create a non-root user 'builder' for OpenWrt safety checks
RUN useradd -m builder && \
    echo "builder ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/builder
