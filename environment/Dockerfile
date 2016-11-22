# DO NOT EDIT, This Dockerfile is generated from ./tools/90_generate_dev_Dockerfile.sh
FROM bjodah/bjodahimg16:v1.2
MAINTAINER Björn Dahlgren <bjodah@DELETEMEgmail.com>
RUN \
    python2 -m pip install --upgrade pip && \
    python3 -m pip install --upgrade pip && \
    python2 -m pip install git+https://github.com/bjodah/cyipopt.git && \
    python3 -m pip install git+https://github.com/bjodah/cyipopt.git && \
    apt-get update && apt-get --quiet --assume-yes --no-install-recommends install sudo latexmk texlive-math-extra && \
    cd /tmp && \
    for FNAME in miniconda3.sh; do \
        wget --no-verbose "http://hera.physchem.kth.se/~repo/bjodahimg16dev/latest/blobs/$FNAME"; \
    done && \
    bash miniconda3.sh -b -p /opt/miniconda3 && \
    rm miniconda3.sh && \
    PATH=/opt/miniconda3/bin:/home3/common/jobhoc2/jobhoc2/jobhoc2:/home/bjorn/vc/cmdlineqc/cmdlineqc:/home/bjorn/bin:/home/bjorn/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/g09/bsd:/opt/g09/local:/opt/g09/extras:/opt/g09:/opt/gv conda config --set always_yes yes && \
    PATH=/opt/miniconda3/bin:/home3/common/jobhoc2/jobhoc2/jobhoc2:/home/bjorn/vc/cmdlineqc/cmdlineqc:/home/bjorn/bin:/home/bjorn/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/g09/bsd:/opt/g09/local:/opt/g09/extras:/opt/g09:/opt/gv conda config --set changeps1 no && \
    PATH=/opt/miniconda3/bin:/home3/common/jobhoc2/jobhoc2/jobhoc2:/home/bjorn/vc/cmdlineqc/cmdlineqc:/home/bjorn/bin:/home/bjorn/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/g09/bsd:/opt/g09/local:/opt/g09/extras:/opt/g09:/opt/gv conda config --set show_channel_urls True && \
    PATH=/opt/miniconda3/bin:/home3/common/jobhoc2/jobhoc2/jobhoc2:/home/bjorn/vc/cmdlineqc/cmdlineqc:/home/bjorn/bin:/home/bjorn/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/g09/bsd:/opt/g09/local:/opt/g09/extras:/opt/g09:/opt/gv conda config --add channels conda-forge && \
    PATH=/opt/miniconda3/bin:/home3/common/jobhoc2/jobhoc2/jobhoc2:/home/bjorn/vc/cmdlineqc/cmdlineqc:/home/bjorn/bin:/home/bjorn/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/g09/bsd:/opt/g09/local:/opt/g09/extras:/opt/g09:/opt/gv conda install conda-build python=3.5 gmp numpy scipy matplotlib cython cmake gsl numba pytest ipywidgets mpmath xz tk mpfr openssl sundials sympy pip sqlite && \
    PATH=/opt/miniconda3/bin:/home3/common/jobhoc2/jobhoc2/jobhoc2:/home/bjorn/vc/cmdlineqc/cmdlineqc:/home/bjorn/bin:/home/bjorn/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/g09/bsd:/opt/g09/local:/opt/g09/extras:/opt/g09:/opt/gv conda clean -t && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
