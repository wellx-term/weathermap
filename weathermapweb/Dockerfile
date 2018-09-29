#From 100.125.0.198:20202/hwcse/nodejs:1.0.0 north
#FROM 100.125.17.64:20202/hwcse/nodejs:1.0.0 #east
FROM 100.125.16.65:20202/hwcse/nodejs:1.0.0


RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

WORKDIR /home/apps/
COPY ./app.js ./
COPY ./bin ./bin
COPY ./package.json ./
COPY ./public ./public
COPY ./routes ./routes
COPY ./shutdown.sh ./
COPY ./start.sh ./
COPY ./views ./views


ENTRYPOINT ["sh", "/home/apps/start.sh"]
