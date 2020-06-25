FROM centos/devtoolset-7-toolchain-centos7

USER 0
RUN yum install -y epel-release https://repo.ius.io/ius-release-el7.rpm \
        && yum install -y git224 \
        && yum clean all -y
RUN USER=default && GROUP=default && \
    curl -SsL https://github.com/boxboat/fixuid/releases/download/v0.5/fixuid-0.5-linux-amd64.tar.gz | tar -C /usr/local/bin -xzf - && \
    chown root:root /usr/local/bin/fixuid && \
    chmod 4755 /usr/local/bin/fixuid && \
    mkdir -p /etc/fixuid && \
    printf "user: $USER\ngroup: $GROUP\n" > /etc/fixuid/config.yml
USER default:default
ENTRYPOINT ["fixuid", "-q"]
