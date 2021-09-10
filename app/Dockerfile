# syntax=docker/dockerfile:1
FROM node:12-alpine
RUN apk add --no-cache python g++ make
WORKDIR /app
COPY . .
RUN yarn config set registry https://registry.npm.taobao.org
RUN yarn install --network-timeout 100000 --production
CMD ["node", "src/index.js"]
