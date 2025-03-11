FROM node:23-alpine3.20
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
EXPOSE 8080
# Add user kubenews with no home directory and no password
RUN adduser -D -H -s /bin/false kubenews
USER kubenews
CMD [ "node", "server.js" ]