FROM ubuntu:16.04

EXPOSE 8000
COPY backend-example-docker ./backend-example-docker
WORKDIR /backend-example-docker
RUN apt-get update > /dev/null
RUN apt-get install -y curl > /dev/null
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs > /dev/null
RUN node -v && npm -v
RUN pwd && ls
RUN npm install
RUN npm update
ENV FRONT_URL=http://localhost:5000
ENTRYPOINT ["npm", "start"]
