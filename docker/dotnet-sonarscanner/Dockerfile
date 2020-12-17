FROM mcr.microsoft.com/dotnet/sdk:3.1

RUN apt-get update && apt-get install unzip && apt-get clean
RUN curl -fL --output /tmp/sonarqube.zip https://github.com/SonarSource/sonar-scanner-msbuild/releases/download/5.0.4.24009/sonar-scanner-msbuild-5.0.4.24009-netcoreapp2.0.zip && \
    mkdir /tmp/sonarqube && cd /tmp/sonarqube && unzip ../sonarqube.zip && \
    dotnet tool install dotnet-sonarscanner --version 4.8.0 --tool-path /opt/dotnet/tools && \
    cd && rm -rf /tmp/sonarqube.zip /tmp/sonarqube

ENV PATH="/opt/dotnet/tools:$PATH"

