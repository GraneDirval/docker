FROM node:latest

RUN npm install -g http-server

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

ARG HOST
ENV HOST $HOST

ARG PORT
ENV PORT $PORT

RUN npm run dev

EXPOSE ${PORT}
#CMD [ "http-server", "dist" ]
