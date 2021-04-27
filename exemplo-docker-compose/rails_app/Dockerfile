FROM ruby:2.5.8

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /rails_app
WORKDIR /rails_app

COPY Gemfile /rails_app/Gemfile
COPY Gemfile.lock /rails_app/Gemfile.lock

RUN bundle install

COPY . /rails_app

EXPOSE 3000

CMD [ "bundle", "exec", "rails", "-b", "0.0.0.0", "-p", "3000" ]