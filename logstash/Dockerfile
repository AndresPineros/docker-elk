# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash-oss:6.2.2
ENV ES_HOST elasticsearch
ENV ES_PORT 9200
ENV TIMEOUT 10

RUN curl https://gist.githubusercontent.com/AndresPineros/4be2dc6877906ff5df4027914fd81d0a/raw/7b33db42ba982673c7ea36adaa1f99bbc9d3562b/wait-centos.sh > /tmp/wait.sh && \
    chmod +x /tmp/wait.sh

CMD bash /tmp/wait.sh $ES_HOST $ES_PORT $TIMEOUT 5 && \
    bash /usr/local/bin/docker-entrypoint

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
