FROM ruby:2.6

WORKDIR /workspaces

COPY Gemfile /workspaces/
COPY Gemfile.lock /workspaces/

RUN bundle install

RUN gem install solargraph && yard gems