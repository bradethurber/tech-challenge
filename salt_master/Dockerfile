FROM ubuntu:trusty
MAINTAINER Joseph D. Marhee <joseph@marhee.me>

RUN apt-get update && apt-get install -y salt-master

COPY setup.sh /opt/setup.sh

ENTRYPOINT ["sh","/opt/setup.sh"]
CMD []
