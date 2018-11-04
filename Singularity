Bootstrap: docker
From: continuumio/miniconda3:4.5.4

%labels
   AUTHOR schmeier@tuta.io

%environment
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This sets global environment variables for anything run within the container
  export PATH="/opt/conda/bin:/usr/local/bin:/usr/bin:/bin:"
  unset CONDA_DEFAULT_ENV
  export ANACONDA_HOME=/opt/conda


%post
   export PATH=/opt/conda/bin:$PATH
   echo "We add conda channels."
   conda config --add channels defaults
   conda config --add channels conda-forge
   conda config --add channels bioconda
   echo "We install tools."
   conda install --yes snakemake=5.3.0
   conda install --yes pandas=0.23.4
   conda install --yes bioconductor-edger=3.20.7
   conda install --yes bioconductor-deseq2=1.18.1
   conda install --yes r-readr=1.1.1
   conda install --yes bioconductor-tximport=1.6.0
   conda install --yes r-samr=2.0
   conda install --yes bioconductor-limma=3.34.9
   conda install --yes bioconductor-ihw=1.6.0
   conda install --yes bioconductor-biocparallel=1.12.0
   conda install --yes bioconductor-clusterprofiler=3.6.0
   conda install --yes bioconductor-org.hs.eg.db=3.5.0
   conda install --yes bioconductor-org.mm.eg.db=3.5.0
   conda install --yes bioconductor-gseabase=1.40.0
   conda clean --index-cache --tarballs --packages --yes