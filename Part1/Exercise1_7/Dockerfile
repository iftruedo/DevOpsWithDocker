FROM ubuntu:16.04

RUN apt-get update > /dev/null && apt-get install -y curl > /dev/null
COPY script.sh .
RUN ls
RUN ["chmod","+x","./script.sh"]
CMD ./script.sh
