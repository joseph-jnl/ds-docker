FROM jupyter/datascience-notebook

# Install Java

RUN su - \
    echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" | tee /etc/apt/sources.list.d/webupd8team-java.list \
    echo "deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" | tee -a /etc/apt/sources.list.d/webupd8team-java.list \
    apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EEA14886 \
    apt-get update \
    apt-get install oracle-java8-installer

# Additional Conda packages
RUN conda install --quiet --yes \
    'psycopg2=2.7*' \
    'pymysql=0.7.9' \
    'pytest=3.1.2' \
    'gcc' \
    'swig' \
    'colorama' \

    && conda install --quiet --yes --channel conda-forge \
    'altair' \
    'scrapy' \
    'icu=58' \
    'xgboost=0.6a2' \
    'opencv' \
    'cookiecutter' \
    'category_encoders' \
    'pymc3' \

    && conda install -c glemaitre imbalanced-learn \

    && conda clean -tipsy

# Install packages not in conda
RUN pip install \
    'kaggle-cli' \
    'scikit-plot' \
    'grip' \
    'pyflux' \
    'scikits.bootstrap' \
    'missingno' \
    'fancyimpute' \
    'awscli' \
    'https://h2o-release.s3.amazonaws.com/h2o/rel-weierstrass/2/Python/h2o-3.14.0.2-py2.py3-none-any.whl'

RUN git clone http://github.com/civisanalytics/python-glmnet.git \
    && cd python-glmnet \
    && python setup.py install -q

RUN ln -s /home/jovyan/ds-toolkit/dstk /opt/conda/lib/python3.6/site-packages

