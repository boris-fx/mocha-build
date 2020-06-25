FROM centos/devtoolset-7-toolchain-centos7

USER 0
RUN yum install -y epel-release https://repo.ius.io/ius-release-el7.rpm \
        && yum install -y git224 \
        && yum clean all -y
USER 1001
