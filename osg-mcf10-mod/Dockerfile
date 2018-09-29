FROM opensciencegrid/osgvo-el7

MAINTAINER Mats Rynge <rynge@isi.edu>

RUN wget -nv -O ~/miniconda.sh http://repo.continuum.io/miniconda/Miniconda3-4.5.1-Linux-x86_64.sh && \
    bash ~/miniconda.sh -b -f -p /opt/conda && \
    export PATH=/opt/conda/bin:$PATH && \
    conda install --yes anaconda && \
    conda install --yes -c conda-forge assimulo && \
    conda install --yes -c conda-forge numpy pandas && \
    conda install --yes -c conda-forge xlrd

# make sure we have a stashcp in the path
RUN ln -f -s /cvmfs/oasis.opensciencegrid.org/osg/modules/stashcp/5.1.2/bin/stashcp /usr/bin/stashcp

# build info
RUN echo "Timestamp:" `date --utc` | tee /image-build-info.txt

