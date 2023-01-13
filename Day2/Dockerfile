FROM ubuntu:20.04

WORKDIR /opt/facebooc

COPY ./facebooc ./opt/facebooc

RUN apt-get update && apt-get install -yq build-essential make libsqlite3-dev sqlite3 && \
    rm -rf /var/lib/apt/lists/* && \
    apt clean

RUN make all

EXPOSE 16000

CMD ["bin/facebooc"]
