FROM python:3.8-slim-buster

LABEL description="Image with Python and tools for cryptography"
LABEL maintainer="Dmitry Kuznetsov <dimitrij.kuznetsov@gmail.com>"


ARG username=ctf
ARG userhome=/home/${username}


RUN useradd \
    -m \
    -s /bin/bash \
    ${username}

RUN apt-get update && apt-get -y install \
    sudo \
    vim \
    wget \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --no-cache-dir --upgrade pip && \
    pip3 install --no-cache-dir \
        ciphey==5.10.0 \
        pycryptodome==3.9.9 \
        jupyter==1.0.0


USER ${username}

ENV USER=${username}
ENV HOME=${userhome}

WORKDIR ${userhome}

ENTRYPOINT ["/bin/bash", "-i"]
