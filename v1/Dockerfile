# This start from the base and apt-get relevant software and library

FROM ubuntu:12.04
MAINTAINER Jimmy Chu <jimmychu@hkwtf.com>

# Update the linux base
RUN apt-get update -q && \
    apt-get install -qy build-essential openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev ncurses-dev automake libtool bison subversion pkg-config libpq5 libpq-dev libcurl4-gnutls-dev python-software-properties libffi-dev libgdbm-dev nano supervisor openssh-server

