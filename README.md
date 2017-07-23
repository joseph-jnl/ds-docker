# ds-docker

Customized data science docker image based on: [jupyter/docker-stacks/datascience-notebook/](https://github.com/jupyter/docker-stacks/tree/master/datascience-notebook)

Additions:

**Visualization**
* altair
* scikit-plot

**ETL**
* scrapy
* psycopg2=2.7*
* pymysql=0.7.9
* kaggle-cli

**Machine Learning**
* xgboost=0.6a
* opencv
* imblearn
* pyflux
* glmnet

**Unit Testing**
* pytest=3.1.2

**Utility**
* grip

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
