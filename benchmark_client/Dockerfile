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
RUN chmod +x /binary/benchmark

WORKDIR /binary

EXPOSE 50051

CMD ./benchmark -address localhost:50051 -nthreads 1 -nrequests 1 -nchannels 1 -concurrency 1 -id benchmark.Benchmark.SimpleCall

