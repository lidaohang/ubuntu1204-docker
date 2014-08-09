FROM jimmychu0807/ubuntu1204:v2
MAINTAINER Jimmy Chu <jimmychu@hkwtf.com>

ADD .ssh/id_docker.pub /root/.ssh/
WORKDIR /root/.ssh
RUN cat id_docker.pub >> authorized_keys

EXPOSE 22
RUN mkdir /var/run/sshd
CMD ["/usr/sbin/sshd", "-D"]
