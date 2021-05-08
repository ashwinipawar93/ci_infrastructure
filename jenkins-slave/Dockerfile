FROM jenkins/slave:3.27-1-alpine

USER root

RUN apk update \
  && apk add curl docker jq shadow tzdata \
  && usermod -aG docker jenkins \
  && rm -rf /var/cache/apk/*

ENV TZ Europe/Berlin
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

