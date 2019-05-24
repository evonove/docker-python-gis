FROM python:3.7

# Base image for python applications using libgeos and libproj
MAINTAINER Evoniners <dev@evonove.it>

# Needed for pip
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8

# Packages
RUN apt-get update -qq && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    binutils \
    gdal-bin \
    libproj-dev \
    libgeos-dev \
    netcat \
 > /dev/null && rm -rf /var/lib/apt/lists/*

RUN pip3 install --quiet --upgrade setuptools

# Directory where the code will be
RUN mkdir -p /code
