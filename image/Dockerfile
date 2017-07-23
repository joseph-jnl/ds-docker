FROM jupyter/datascience-notebook

# Additional Conda packages
RUN conda install --quiet --yes --channel conda-forge \
    'altair' \
    'scrapy' \
    'icu=58' \
    'xgboost=0.6a2' \
    'opencv' \
    'glmnet'
    
    && conda install --quiet --yes \
    'psycopg2=2.7*' \
    'pymysql=0.7.9' \
    'pytest=3.1.2' \

    && conda install -c glemaitre imbalanced-learn \

    && conda clean -tipsy

# Install packages not in conda
RUN pip install \
    'kaggle-cli' \
    'scikit-plot' \
    'grip' \
    'pyflux'

