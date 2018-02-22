FROM elasticsearch:2.4.5

RUN bin/plugin install io.fabric8/elasticsearch-cloud-kubernetes/2.4.5_01
RUN bin/plugin install lmenezes/elasticsearch-kopf/2.1.2
RUN bin/plugin install cloud-aws
RUN bin/plugin install https://github.com/elastic/elasticsearch-migration/releases/download/v2.0.4/elasticsearch-migration-2.0.4.zip

ENV BOOTSTRAP_MLOCKALL=false
ENV JAVA_OPTS=-Djava.net.preferIPv4Stack=true

# common dependencies
RUN apt-get update && apt-get install -y \
        jq \
        curl \
    && rm -rf /var/lib/apt/lists/*

ADD elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
