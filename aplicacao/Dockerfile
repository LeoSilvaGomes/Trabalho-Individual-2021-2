FROM ruby:3.0.0

RUN apt-get update -qq
RUN apt-get install -y nodejs postgresql-client

WORKDIR /src

COPY Gemfile /src/Gemfile
COPY Gemfile.lock /src/Gemfile.lock

RUN bundle install

CMD ["rails", "server", "0.0.0.0"]