FROM python:3.8-slim

# Install build tools and libraries required for compilation
RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    python3-dev \
    zlib1g-dev \
    libbz2-dev \
    liblzma-dev \
    libcurl4-openssl-dev \
    libssl-dev \
    make \
    procps \
    && rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade pip

RUN pip install --no-cache-dir \
    numpy==1.24.4 \
    scipy==1.10.1 \
    pandas==1.5.3 \
    matplotlib==3.7.5 \
    biopython==1.83 \
    hdx-python-country==3.5.0 \
    pysam==0.22.0

ENTRYPOINT ["python3"]