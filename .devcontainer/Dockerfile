# syntax=docker/dockerfile:1

FROM ghcr.io/oracle/oraclelinux:9-slim

RUN microdnf -y update && \
    microdnf -y install python3.11 && \
    microdnf -y install python3.11-devel && \
    microdnf -y install openldap-devel && \
    microdnf -y install gcc && \
    microdnf -y install gcc-c++ && \
    microdnf -y install autoconf && \
    microdnf -y install memcached && \
    microdnf -y install mariadb-connector-c-devel && \
    microdnf -y install gettext && \
    microdnf -y install glibc-langpack-pt systemd cronie && \
    microdnf -y install git && \
    microdnf -y clean all && \
    systemctl enable crond.service

#set environment variables
ENV LANG=pt_BR.UTF-8
ENV LC_ALL=pt_BR.UTF-8
ENV TZ="America/Sao_Paulo"
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

CMD ["bash"]
