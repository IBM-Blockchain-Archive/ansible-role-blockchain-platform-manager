#
# SPDX-License-Identifier: Apache-2.0
#
FROM alpine:3.10
RUN apk add --no-cache ansible jq moreutils && \
    pip3 install docker
RUN wget -qO docker-19.03.2.tgz https://download.docker.com/linux/static/stable/x86_64/docker-19.03.2.tgz && \
    tar xzvf docker-19.03.2.tgz --strip 1 -C /usr/local/bin docker/docker && \
    rm docker-19.03.2.tgz && \
    wget -qO /usr/local/bin/docker-compose "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" && \
    chmod +x /usr/local/bin/docker-compose
RUN mkdir /lib64 && \
    ln -s /lib/libc.musl-x86_64.so.1 /lib64/ld-linux-x86-64.so.2 && \
    wget -qO fabric-bins.tar.gz https://nexus.hyperledger.org/content/repositories/releases/org/hyperledger/fabric/hyperledger-fabric/linux-amd64-1.4.3/hyperledger-fabric-linux-amd64-1.4.3.tar.gz && \
    tar xvf fabric-bins.tar.gz -C /usr/local && \
    wget -qO fabric-ca-bins.tar.gz https://nexus.hyperledger.org/content/repositories/releases/org/hyperledger/fabric-ca/hyperledger-fabric-ca/linux-amd64-1.4.3/hyperledger-fabric-ca-linux-amd64-1.4.3.tar.gz && \
    tar xvf fabric-ca-bins.tar.gz -C /usr/local && \
    rm fabric-bins.tar.gz fabric-ca-bins.tar.gz
ENV FABRIC_CFG_PATH=/usr/local/config
COPY ansible-role-blockchain-platform-manager.tar.gz /usr/local/src/
RUN mkdir -p /etc/ansible/roles/ibm.blockchain_platform_manager && \
    cd /etc/ansible/roles/ibm.blockchain_platform_manager && \
    tar xf /usr/local/src/ansible-role-blockchain-platform-manager.tar.gz