FROM node:8-alpine
RUN apk update && apk add git && rm -rf /var/cache/apk/*
WORKDIR /app
COPY . /app/
RUN npm install
RUN node_modules/.bin/bower --allow-root --no-color -q install
ENTRYPOINT [ "node", "server.js" ]
