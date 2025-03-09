FROM node:20
RUN mkdir -p /opt/server
EXPOSE 8080
ENV DB_HOST="localhost"
WORKDIR /opt/server
COPY expense-backend/*.js .
COPY expense-backend/package.json .
RUN npm install
CMD [ "node", "index.js"]