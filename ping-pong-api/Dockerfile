FROM node:13-alpine
RUN mkdir -p /app
COPY . /app
WORKDIR /app
RUN npm install
CMD ["node", "server.js", "&", ":", "echo", "$dev"]
