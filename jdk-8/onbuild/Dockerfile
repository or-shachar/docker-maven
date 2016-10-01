FROM maven:3-jdk-8

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY *pom.xml /usr/src/app/
ONBUILD RUN mvn dependency:get

ONBUILD ADD . /usr/src/app
ONBUILD RUN mvn install
