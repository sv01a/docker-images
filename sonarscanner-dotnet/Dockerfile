FROM mcr.microsoft.com/dotnet/sdk:8.0.204-alpine3.19

ENV PATH="${PATH}:/root/.dotnet/tools"

RUN apk add --update openjdk17 && \
    rm -rf /var/cache/apk/* && \
    dotnet tool install --global dotnet-sonarscanner