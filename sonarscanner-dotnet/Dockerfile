FROM mcr.microsoft.com/dotnet/core/sdk:3.1-alpine

ENV PATH="${PATH}:/root/.dotnet/tools"
ENV JAVA_HOME="/usr/lib/jvm/java-1.8-openjdk"

RUN apk add --update openjdk8-jre && \
    rm -rf /var/cache/apk/* && \
    dotnet tool install --global dotnet-sonarscanner