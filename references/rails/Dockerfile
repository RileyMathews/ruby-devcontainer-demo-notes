FROM ruby:2.6

RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs

WORKDIR /workspaces

COPY Gemfile /workspaces/
COPY Gemfile.lock /workspaces/

RUN bundle install
RUN gem install solargraph && yard gems

COPY . /workspaces/
EXPOSE 3000
CMD ["rails", "s", "-b", "0.0.0.0"]