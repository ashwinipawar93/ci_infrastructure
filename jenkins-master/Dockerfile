FROM jenkins/jenkins:2.277.2-lts-alpine

USER root
RUN apk update \
    && apk add --no-cache curl docker jq tzdata \
    && rm -rf /var/cache/apk/*

ENV TZ Europe/Berlin
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY plugins.txt /usr/share/jenkins/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt

USER jenkins

