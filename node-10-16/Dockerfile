FROM node:10.16.3

WORKDIR /app/

COPY package.json ./
RUN npm install --silent --no-cache --registry=https://registry.npm.taobao.org

COPY ./ ./

RUN npm run fetch:blocks

CMD ["npm", "run", "start"]