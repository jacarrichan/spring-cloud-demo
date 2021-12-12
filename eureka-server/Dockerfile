FROM anapsix/alpine-java:8_server-jre_unlimited


ENV TZ=Asia/Shanghai

RUN ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone


EXPOSE 8761

ARG JAR_FILE
COPY ${JAR_FILE} app.jar

CMD java -Djava.security.egd=file:/dev/./urandom -jar /app.jar
