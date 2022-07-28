FROM continuumio/anaconda3

ADD ./data/anaconda/conf/requirements.txt /

RUN apt-get update && apt-get upgrade -y && apt-get -y install gcc && pip install --upgrade setuptools && pip install -r requirements.txt
RUN mkdir -p /root/.jupyter
COPY ./data/anaconda/conf/jupyter_notebook_config.json /root/.jupyter/jupyter_notebook_config.json

EXPOSE 8888