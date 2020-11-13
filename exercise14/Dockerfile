FROM ruby:2.6.0
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_15.x
RUN apt-get install -y nodejs
COPY . .
RUN bundle install
RUN rails db:migrate
EXPOSE 3000
CMD rails s