FROM jupyter/datascience-notebook

# Additional Conda packages
RUN conda install --quiet --yes --channel conda-forge \
    'altair' \
    'scrapy' \
    'xgboost=0.6a2' && \
    conda install --quiet --yes \
    'psycopg2=2.7*' \
    'pymysql=0.7.9' \
    && conda clean -tipsy

# Install packages not in conda
RUN pip install kaggle-cli
