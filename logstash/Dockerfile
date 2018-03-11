# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash-oss:6.2.2

RUN logstash-plugin install x-pack

ENV ES_HOST elasticsearch
ENV ES_PORT 9200
ENV TIMEOUT 120

RUN curl https://gist.githubusercontent.com/AndresPineros/4be2dc6877906ff5df4027914fd81d0a/raw/d20ae9470b028584a11a6f9f4e04fe6186c5bcc1/wait-centos.sh > /tmp/wait.sh && \
    chmod +x /tmp/wait.sh

CMD bash /tmp/wait.sh $ES_HOST $ES_PORT $TIMEOUT 5 && \
    bash /usr/local/bin/docker-entrypoint

