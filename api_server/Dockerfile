FROM ubuntu:16.10

ADD . /api_server

ADD lib/libgrpc++.so /usr/local/lib
ADD lib/libgrpc.so /usr/local/lib

RUN ldconfig

WORKDIR /api_server

EXPOSE 50051

ENTRYPOINT ./apiserver --config config/benchmark.config --proto config/benchmark.proto

