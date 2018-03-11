FROM docker.elastic.co/beats/filebeat:6.2.2

RUN curl https://gist.githubusercontent.com/AndresPineros/4be2dc6877906ff5df4027914fd81d0a/raw/7b33db42ba982673c7ea36adaa1f99bbc9d3562b/wait-centos.sh > /tmp/wait.sh && \
    chmod +x /tmp/wait.sh

ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
CMD ["-e"]