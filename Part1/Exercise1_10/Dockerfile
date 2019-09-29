FROM ubuntu:16.04

EXPOSE 5000
COPY frontend-example-docker ./frontend-example-docker
WORKDIR /frontend-example-docker
RUN apt-get update > /dev/null
RUN apt-get install -y curl > /dev/null
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs > /dev/null
RUN node -v && npm -v
RUN pwd && ls
RUN npm install
RUN npm update
ENTRYPOINT ["npm", "start"]
