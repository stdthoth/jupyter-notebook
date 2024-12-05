# Use the official Ubuntu base image
FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    sudo \
    python3-pip \
    python3-dev \
    python3-venv \
    curl \
    git \
    build-essential \
    libssl-dev \
    libffi-dev \
    libbz2-dev \
    libreadline-dev \
    libsqlite3-dev \
    wget \
    tk-dev \
    libncurses5-dev \
    libgdbm-dev \
    libc6-dev \
    liblzma-dev \
    zlib1g-dev \
    libyaml-dev \
    && apt-get clean

RUN pip install jupyterlab numpy pandas matplotlib seaborn scikit-learn

EXPOSE 8888

CMD ["jupyter", "lab", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''"]
