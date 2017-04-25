FROM ubuntu:16.10

#RUN apt-get update 
# && apt-get install -y --force-yes --no-install-recommends \
#      apt-transport-https \
#      curl \
#      ca-certificates \
# && apt-get clean \
# && apt-get autoremove \
# && rm -rf /var/lib/apt/lists/*


ADD . /binary
RUN chmod +x /binary/apiserver

WORKDIR /binary

EXPOSE 50051

CMD ./apiserver --config benchmark.config --proto benchmark.proto

