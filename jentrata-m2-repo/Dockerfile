FROM jentrata/maven

MAINTAINER "Aaron Walker" <aaronpwalker@gmail.com>

ENV APP_GIT_REPO https://github.com/aaronwalker/jentrata-msh.git

ADD m2-repo/ /var/maven/.m2/repository

RUN mkdir /tmp/app && git clone $APP_GIT_REPO /tmp/app
RUN cd /tmp/app && /usr/share/java/maven/bin/mvn clean install -DskipTests
RUN rm -rf /tmp/app

VOLUME ["/var/maven"]
