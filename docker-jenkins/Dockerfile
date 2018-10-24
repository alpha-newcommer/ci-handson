FROM jenkins/jenkins:2.147

USER root

RUN  apt-get update \
    && apt-get install -y git \
      lsb-release \
      apt-transport-https \
      ca-certificates \
      curl \
      gnupg2 \
      software-properties-common \
    && apt-get install --no-install-recommends -y openssh-server \
    && curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add - \
    && add-apt-repository \
       "deb [arch=amd64] https://download.docker.com/linux/debian \
       $(lsb_release -cs) \
       stable" \
    && apt-get update \
    && apt-get install -y docker-ce

# add docker group
RUN addgroup -S docker && adduser jenkins docker

USER jenkins
