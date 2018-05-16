FROM opensciencegrid/osgvo-el7

MAINTAINER Mats Rynge <rynge@isi.edu>

RUN wget -nv -O ~/miniconda.sh http://repo.continuum.io/miniconda/Miniconda3-4.5.1-Linux-x86_64.sh && \
    bash ~/miniconda.sh -b -f -p /opt/miniconda && \
    export PATH=/opt/miniconda/bin:$PATH && \
    conda install --yes anaconda && \
    conda install --yes -c conda-forge assimulo && \
    conda install --yes -c conda-forge numpy pandas && \
    conda install --yes -c conda-forge xlrd

# build info
RUN echo "Timestamp:" `date --utc` | tee /image-build-info.txt

