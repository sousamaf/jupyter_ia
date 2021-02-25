# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
# Para utilizar com GPU
ARG BASE_CONTAINER=tensorflow/tensorflow:latest-gpu-jupyter

# Para utilizar com CPU
#ARG BASE_CONTAINER=tensorflow/tensorflow

FROM $BASE_CONTAINER

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

# Install Tensorflow
# RUN pip install --quiet --no-cache-dir \
#     'tensorflow-gpu==2.3.0' && \
#     fix-permissions "${CONDA_DIR}" && \
#     fix-permissions "/home/${NB_USER}"
#RUN pip install tensorboard

RUN pip install SpeechRecognition
RUN pip install --user -U nltk
RUN pip install fuzzywuzzy
RUN pip install pandas_datareader
RUN pip install gym
RUN pip install Keras

USER root
RUN python -m nltk.downloader -d /usr/local/share/nltk_data all
#USER jovyan
