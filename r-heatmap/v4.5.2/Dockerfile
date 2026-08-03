# R with packages:
# - ggplot2
# - dplyr
# - gplots
# - pheatmap
# https://cran.r-project.org/
# v4.5.2

FROM rocker/r-ver:4.5.2

LABEL maintainer=kevin.da-silva@pasteur.fr

ENV CRANREPO="https://cloud.r-project.org/"
ENV RLIBPATH="/usr/local/lib/R/site-library/"

COPY install.R /
COPY packages.txt /

# Install system dependencies required by the R packages
RUN apt-get update && apt-get install -y \
    libcurl4-openssl-dev \
    libssl-dev \
    libxml2-dev \
    libsqlite3-dev \
    zlib1g-dev \
    && rm -rf /var/lib/apt/lists/*

RUN Rscript /install.R $CRANREPO $RLIBPATH /packages.txt

CMD ["R"]
