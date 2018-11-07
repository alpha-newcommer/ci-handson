FROM jenkins/jenkins:2.147

USER root

# docker install
RUN apt update -y \
    && apt install -y \
       apt-transport-https \
       ca-certificates \
       curl \
       software-properties-common \
       git \
    && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - \
    && add-apt-repository \
       "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
       xenial \
       stable" \
    && apt update -y \
    && apt install -y docker-ce


USER jenkins
