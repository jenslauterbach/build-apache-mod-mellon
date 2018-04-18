FROM centos:centos7.4.1708

ENV MELLON_VERSION=0.14.0

RUN \
    yum install -y \
        gcc \
        httpd-devel \
        lasso-devel \
        libcurl-devel \
        make \
    && \
    curl -L https://github.com/UNINETT/mod_auth_mellon/releases/download/v${MELLON_VERSION}/mod_auth_mellon-${MELLON_VERSION}.tar.gz | tar -xvzC /tmp && \
    cd /tmp/mod_auth_mellon-${MELLON_VERSION} && \
    ./configure --enable-diagnostics && \
    make && \
    make install