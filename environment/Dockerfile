# DO NOT EDIT, This Dockerfile is generated from ./tools/90_generate_dev_Dockerfile.sh
FROM bjodah/bjodahimg16:v1.2
MAINTAINER Björn Dahlgren <bjodah@DELETEMEgmail.com>
ENV PATH /opt/miniconda3/bin:$PATH
RUN \
    cd /tmp && \
    for FNAME in miniconda3.sh; do \
        wget --no-verbose "http://hera.physchem.kth.se/~repo/bjodahimg16dev/latest/blobs/$FNAME"; \
    done && \
    bash miniconda3.sh -b -p /opt/miniconda3 && \
    rm miniconda3.sh && \
    conda config --set always_yes yes && \
    conda config --set changeps1 no && \
    conda config --set show_channel_urls True && \
    conda config --add channels conda-forge && \
    conda install conda-build python=3.5 gmp numpy scipy matplotlib cython cmake gsl numba && \
    conda clean -t && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN \
    python2 -m pip install git+https://github.com/bjodah/cyipopt.git &&     python3 -m pip install git+https://github.com/bjodah/cyipopt.git &&     conda install pytest
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
