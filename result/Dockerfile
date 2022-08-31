FROM node:8.9-alpine
WORKDIR /app
COPY . .
RUN npm install -g nodemon
RUN npm config set registry https://registry.npmjs.org

RUN npm install && npm ls && npm cache clean --force && mv /app/node_modules /node_modules
EXPOSE 4000
CMD ["node","server.js"]

