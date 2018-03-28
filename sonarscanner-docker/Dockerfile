FROM java:alpine
ENV SONAR_SCANNER_VERSION 3.1.0.1141-linux
ENV SONAR_SCANNER_PATH /sonar-scanner-${SONAR_SCANNER_VERSION}
RUN apk add --no-cache wget && \
    wget https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${SONAR_SCANNER_VERSION}.zip -O sonar-scanner.zip && \
    unzip sonar-scanner.zip && \
    rm -rf sonar-scanner.zip ${SONAR_SCANNER_PATH}/jre && \
    sed -i 's/use_embedded_jre=true/use_embedded_jre=false/g' ${SONAR_SCANNER_PATH}/bin/sonar-scanner && \
    cd /usr/bin && ln -s ${SONAR_SCANNER_PATH}/bin/sonar-scanner sonar-scanner && \
    apk del wget
CMD sonar-scanner
