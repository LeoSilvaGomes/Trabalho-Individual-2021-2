FROM ruby:3.0.0

RUN apt-get update -qq && apt-get install -y nodejs postresql-client

WORKDIR /app

COPY Gemfile /aplicacao/Gemfile
COPY Gemfile.lock /aplicacao/Gemfile.lock

RUN bundle install

CMD ["rails", "server", "0.0.0.0"]