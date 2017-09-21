FROM jupyter/datascience-notebook

# Additional Conda packages
RUN conda install --quiet --yes \
    'psycopg2=2.7*' \
    'pymysql=0.7.9' \
    'pytest=3.1.2' \
    'gcc' \
    'swig' \
    'h2o' \

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
    'awscli'

RUN git clone http://github.com/civisanalytics/python-glmnet.git \
    && cd python-glmnet \
    && python setup.py install -q

RUN ln -s /home/jovyan/ds-toolkit/dstk /opt/conda/lib/python3.6/site-packages

