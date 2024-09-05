FROM jenkins/inbound-agent:latest-jdk11
MAINTAINER Aruna Indonesia Tech. <aruna-devops@aruna.id>

ENV HELM_VERSION v3.15.1
ENV HELM_FILENAME helm-${HELM_VERSION}-linux-amd64.tar.gz
ENV KUBE_LATEST_VERSION="v1.31.0"

USER root
WORKDIR /
RUN apt-get update && apt-get install -y curl tar gzip ca-certificates git rsync make
RUN curl -L https://get.helm.sh/${HELM_FILENAME} | tar zxv -C /tmp \
  && cp /tmp/linux-amd64/helm /usr/local/bin/helm \
  && chmod +x /usr/local/bin/helm

RUN curl -L https://storage.googleapis.com/kubernetes-release/release/${KUBE_LATEST_VERSION}/bin/linux/amd64/kubectl -o /usr/local/bin/kubectl \
 && chmod +x /usr/local/bin/kubectl

USER jenkins
