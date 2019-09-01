FROM wql425/openjdk:latest
MAINTAINER Darrell
LABEL name="gradle" version="4.10" description="Gradle"

ENV GRADLE_VERSION="gradle-4.10"
ENV GRADLE=/gradle/$GRADLE_VERSION/bin
ENV PATH=$PATH:$GRADLE

WORKDIR /gradle/
RUN yum install -y unzip && yum clean all \
    && curl -o gradle.zip https://downloads.gradle.org/distributions/$GRADLE_VERSION-bin.zip && unzip ./gradle.zip \
    && rm -f gradle.zip
