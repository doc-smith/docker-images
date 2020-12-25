FROM python:3.8-slim-buster

LABEL description="Image with Python and tools for cryptography"
LABEL maintainer="Dmitry Kuznetsov <dimitrij.kuznetsov@gmail.com>"


RUN apt-get update && apt-get -y install \
    sudo \
    vim \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --no-cache-dir --upgrade pip && \
    pip3 install --no-cache-dir \
        ciphey==5.10.0 \
        pycryptodome==3.9.9 \
        jupyter==1.0.0


ENTRYPOINT ["/bin/bash", "-i"]
