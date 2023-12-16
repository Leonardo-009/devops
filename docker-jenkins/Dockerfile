FROM jenkins/jenkins:lts-jdk11

# Defina o usuário root temporariamente
USER root

# Atualize os pacotes do sistema e instale as dependências que você precisa
RUN apt-get update && apt-get install -y \
    software-properties-common

# Atualize os pacotes do sistema e instale as dependências necessárias
RUN apt-get update && apt-get install -y \
    build-essential \
    wget \
    libssl-dev \
    zlib1g-dev \
    libncurses5-dev \
    libncursesw5-dev \
    libreadline-dev \
    libsqlite3-dev \
    libgdbm-dev \
    libdb5.3-dev \
    libbz2-dev \
    libexpat1-dev \
    liblzma-dev \
    tk-dev

# Faça o download do Python 3.8
WORKDIR /tmp
RUN wget https://www.python.org/ftp/python/3.8.12/Python-3.8.12.tgz
RUN tar -xvf Python-3.8.12.tgz

# Compile e instale o Python 3.8
WORKDIR /tmp/Python-3.8.12
RUN ./configure --enable-optimizations
RUN make
RUN make altinstall

# Volte para o usuário do Jenkins
USER jenkins