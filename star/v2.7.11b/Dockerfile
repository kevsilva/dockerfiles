# STAR
# https://github.com/alexdobin/STAR/
# https://anaconda.org/channels/bioconda/packages/star/overview
# v2.7.11b
# Use a minimal Miniconda base image (available for amd64 and arm64)
FROM condaforge/miniforge3:latest

ENV VERSION=2.7.11b

# Install bwa-mem2 from bioconda
RUN conda install -y -c bioconda -c conda-forge star=${VERSION} \
    && conda clean --all --yes

# Set a default working directory
WORKDIR /data

# Set the default command
ENTRYPOINT ["STAR"]
CMD ["--help"]