# https://github.com/zironycho/pytorch-docker/blob/main/1.12.0/Dockerfile

# FROM python:3.8.13-slim-bullseye
FROM nvidia/cuda:11.4.2-cudnn8-devel-ubuntu20.04

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
    # build-essential \
    # # To avoid `Problem with the SSL CA cert (path? access rights?)` on git clone
    # ca-certificates \
    # curl \
    git \
    vim \
    # python3-numpy \
    # python3-pip \
    # python3-setuptools \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspace

COPY ./requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
