# ds-docker

Customized data science docker image based on: [jupyter/docker-stacks/datascience-notebook/](https://github.com/jupyter/docker-stacks/tree/master/datascience-notebook)

Additions:

**Visualization**
* altair
* scikit-plot
* missingno - Missing values visualization

**ETL**
* scrapy - Web scraping
* psycopg2=2.7* - Postgres sqlalchemy driver
* pymysql=0.7.9 - MySQL sqlalchemy driver
* kaggle-cli

**Stats & Machine Learning**
* xgboost=0.6a
* opencv - Image processing
* imblearn - Under/over sampling
* pyflux - Time series forecasting
* glmnet
* scikits.bootstrap
* category_encoders - Alternatives to onehot encoding
* fancyimpute - Alternatives to simple mean/median imputation
* pymc - Bayesian stats
* h2o - java ml algos

**Unit Testing**
* pytest=3.1.2

**Utility**
* grip
* cookiecutter - Project templates
* awscli - Amazon EC2 command line

## Install
Install [docker](https://www.docker.com/community-edition)

Then build:
``` 
sudo docker build -t josephjnl/ds-docker:latest \
https://github.com/joseph-jnl/ds-docker.git#master:image
```

or download image:
``` 
sudo docker pull josephjnl/ds-docker
```
