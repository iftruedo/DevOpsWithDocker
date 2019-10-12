FROM ubuntu:16.04
FROM ruby:2.6.0

EXPOSE 3000
RUN apt-get update > /dev/null
RUN apt-get install -y curl > /dev/null
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs > /dev/null
RUN node -v && npm -v
RUN npm install
COPY ./rails-example-project ./rails-example-project
WORKDIR ./rails-example-project
CMD ["gem","install","bundler"]
RUN bundle install
RUN rails db:migrate
CMD ["rails", "server", "--binding", "0.0.0.0"]
