FROM node:10.16.3

RUN mkdir /app
WORKDIR /app/

COPY package.json ./
RUN npm install --silent --no-cache --registry=https://registry.npm.taobao.org

VOLUME /app

EXPOSE 22 80 8000
CMD ["sh", "-c", "env >> /etc/environment ; /usr/bin/supervisord"]