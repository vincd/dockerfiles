FROM python:3.7-alpine

RUN pip install --upgrade pip

RUN apk --update --no-cache add \
    gcc \
    musl-dev \
    openssl-dev \
    libffi-dev \
    python3-dev \
    git && \
    rm -rf /var/cache/apk/*

RUN mkdir -p /opt/impacket
RUN git clone https://github.com/SecureAuthCorp/impacket.git /opt/impacket
WORKDIR /opt/impacket

RUN pip install .
WORKDIR /opt/impacket/examples
CMD ["python"]
