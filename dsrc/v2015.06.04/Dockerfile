# DSRC
# https://anaconda.org/channels/bioconda/packages/dsrc/overview
# v2015.06.04
# Use a minimal Miniconda base image (available for amd64 and arm64)
FROM condaforge/miniforge3:latest

ENV VERSION=2015.06.04

# Install bwa-mem2 from bioconda
RUN conda install -y -c bioconda -c conda-forge dsrc=${VERSION} \
    && conda clean --all --yes

# Set a default working directory
WORKDIR /data

# Set the default command
ENTRYPOINT ["dsrc"]
CMD ["--help"]