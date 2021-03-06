# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
# Para utilizar com GPU
ARG BASE_CONTAINER=tensorflow/tensorflow:latest-gpu-jupyter

# Para utilizar com CPU
# ARG BASE_CONTAINER=tensorflow/tensorflow

FROM $BASE_CONTAINER

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

RUN apt-get update && apt-get install wget

# Install Tensorflow
# RUN pip install --quiet --no-cache-dir \
#     'tensorflow-gpu==2.3.0' && \
#     fix-permissions "${CONDA_DIR}" && \
#     fix-permissions "/home/${NB_USER}"
RUN apt-get install python-opengl -y
RUN apt-get install -y xvfb ffmpeg -y
RUN python3 -m pip install --upgrade pip
RUN pip install tensorflow
RUN pip install --user tf-agents
RUN pip install --user dm-reverb
RUN pip install -q tensorflow-recommenders
RUN pip install -q --upgrade tensorflow-datasets
RUN pip install 'imageio==2.4.0'
RUN pip install pyvirtualdisplay
RUN pip install tf-agents
RUN pip install Pillow
RUN pip install tensorboard
RUN pip install SpeechRecognition
RUN pip install --user -U nltk
RUN pip install fuzzywuzzy
RUN pip install pandas_datareader
RUN pip install sklearn
RUN pip install scikit-image
RUN pip install gym
RUN pip install Keras
RUN pip install voila
RUN pip install RISE
RUN pip install pydotplus
RUN pip install graphviz
RUN pip install seaborn
RUN pip install simpful 
# RUN pip install atari_py
RUN pip install matplotlib

RUN pip install jupyter-tabnine
RUN jupyter nbextension install --py jupyter_tabnine
RUN jupyter nbextension enable --py jupyter_tabnine
RUN jupyter serverextension enable --py jupyter_tabnine
RUN pip install python-language-server

RUN ipython profile create
RUN echo 'c.IPCompleter.use_jedi = False' >> ~/.ipython/profile_default/ipython_kernel_config.py

## Integração com o Metatrader
# RUN pip install MetaTrader5
# RUN pip install pytz

WORKDIR /tf/
USER root
#RUN python -m nltk.downloader -d /usr/local/share/nltk_data all
#USER jovyan
