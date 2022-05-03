# This dockerfile came from https://docs.docker.com/samples/rails/

FROM ruby:3.0.0

RUN apt-get update -qq && apt-get install -y nodejs postgresql-client

WORKDIR /src

COPY Gemfile /src/Gemfile
COPY Gemfile.lock /src/Gemfile.lock

RUN bundle install

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]
EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]