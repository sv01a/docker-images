FROM microsoft/dotnet:2.2-sdk-alpine

ENV PATH="${PATH}:/root/.dotnet/tools"
ENV JAVA_HOME="/usr/lib/jvm/java-1.8-openjdk"

RUN apk add --update openjdk8-jre && \
    rm -rf /var/cache/apk/* && \
    dotnet tool install --global dotnet-sonarscanner --version 4.4.2