FROM jentrata/maven

MAINTAINER "Aaron Walker" <aaronpwalker@gmail.com>

ENV APP_GIT_REPO https://github.com/aaronwalker/jentrata-msh.git

RUN mkdir /tmp/app && git clone $APP_GIT_REPO /tmp/app
RUN cd /tmp/app && /usr/share/java/maven/bin/mvn clean install -DskipTests
RUN rm -rf /tmp/app

VOLUME ["/var/maven"]
