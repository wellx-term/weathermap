#FROM 100.125.0.198:20202/hwcse/dockerhub-java:8-jre-alpine
#FROM 100.125.17.64:20202/hwcse-cn-east-2/dockerhub-java:8-jre-alpine
FROM 100.125.16.65:20202/hwcse-cn-south-1/dockerhub-java:8-jre-alpine

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

WORKDIR /home/apps/
ADD target/weather-1.0.0.jar .
ADD target/lib ./lib
ADD start.sh .

ENTRYPOINT ["sh", "/home/apps/start.sh"]
