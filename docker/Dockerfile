FROM ubuntu:14.04

MAINTAINER Wise.io, Inc. <help@wise.io>

ENV DEBIAN_FRONTEND noninteractive

# Install packages
RUN apt-get -y update && apt-get install -y wget nano locales curl unzip wget openssl libhdf5-dev

ENV LANGUAGE es_ES.UTF-8
ENV LANG es_ES.UTF-8

RUN locale-gen es_ES.UTF-8
RUN dpkg-reconfigure locales


# Install and setup minimal Anaconda Python distribution
RUN wget http://repo.continuum.io/miniconda/Miniconda-latest-Linux-x86_64.sh -O miniconda.sh
RUN bash miniconda.sh -b -p /anaconda && rm miniconda.sh
ENV PATH /anaconda/bin:$PATH

# Set the time zone to the local time zone
RUN echo "Europe/Madrid" > /etc/timezone && dpkg-reconfigure --frontend noninteractive tzdata

# For image inheritance.
ONBUILD ENV PATH /anaconda/bin:$PATH

# Install some essential data science packages in python, including psycopg2
RUN conda install scipy numpy scikit-learn scikit-image pyzmq nose readline pandas matplotlib seaborn dateutil ipython-notebook nltk pip
RUN conda install psycopg2
RUN conda install cython hdf5 pytables

# Get openpyxl, xlrd, xlwt to read Excel files. Versions compatible with pandas
RUN pip install openpyxl==1.8.6
RUN pip install xlrd
RUN pip install xlwt

# Get tweepy
RUN pip install tweepy

ENV PEM_FILE /key.pem
# $PASSWORD will get `unset` within notebook.sh, turned into an IPython style hash
ENV PASSWORD Dont make this your default
ENV USE_HTTP 1

# Add current files to / and set entry point.
ADD . /workspace
WORKDIR /workspace
ADD notebook.sh /notebook.sh
RUN chmod a+x /notebook.sh

EXPOSE 8888

CMD ["/notebook.sh"]

