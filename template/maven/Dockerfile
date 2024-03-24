FROM zhongruizhi/spark-submit:3.5.1-hadoop3.3.6-amd64

LABEL maintainer="Ruizhi Zhong <ruizhi.zhong@outlook.com>"

ENV SPARK_APPLICATION_JAR_NAME application-1.0
ENV SPARK_APPLICATION_JAR_LOCATION /app/application.jar

COPY template.sh /

RUN apk add --no-cache openjdk17 maven\
      && chmod +x /template.sh \
      && mkdir -p /app \
      && mkdir -p /usr/src/app

# Copy the POM-file first, for separate dependency resolving and downloading
ONBUILD COPY pom.xml /usr/src/app
ONBUILD RUN cd /usr/src/app \
      && mvn dependency:resolve
ONBUILD RUN cd /usr/src/app \
      && mvn verify

# Copy the source code and build the application
ONBUILD COPY . /usr/src/app
ONBUILD RUN cd /usr/src/app \
      && mvn clean package

CMD ["/bin/bash", "/template.sh"]
