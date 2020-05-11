FROM bioconductor/bioconductor_docker:latest

MAINTAINER chapmanbe <brian.chapman@unimelb.edu.au>
USER root

 RUN apt-get update && apt-get upgrade -y && apt-get install -y \
      graphviz\
      vim \
  && rm -rf /var/lib/apt/lists/*

RUN R -e 'install.packages("https://www.bnlearn.com/releases/bnlearn_latest.tar.gz")' && \
    R -e 'install.packages("fmsb")' && \
    R -e 'install.packages("pROC")' && \
    R -e 'BiocManager::install("Rgraphviz")'
