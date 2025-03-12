FROM jenkins/jenkins:lts


USER root


RUN rm -rf /var/lib/dpkg/info && \
    mkdir -p /var/lib/dpkg/info && \
    apt-get update && \
    apt-get install -y make g++ --fix-missing


USER jenkins
