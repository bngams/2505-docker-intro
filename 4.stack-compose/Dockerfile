# syntax=docker/dockerfile:1

FROM node:lts-alpine
WORKDIR /app
COPY package.json .
RUN yarn install --production
COPY . .
CMD ["node", "src/index.js"]
EXPOSE 3000