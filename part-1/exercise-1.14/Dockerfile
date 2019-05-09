FROM ruby:2.6.0
RUN apt-get update && apt-get install -y git nodejs
RUN git clone https://github.com/docker-hy/rails-example-project
WORKDIR /rails-example-project
RUN gem install bundler
RUN bundle install
ENV SECRET_KEY_BASE="bin/rake secret"
RUN rails db:migrate RAILS_ENV=production
RUN rake assets:precompile
CMD rails s -e production
