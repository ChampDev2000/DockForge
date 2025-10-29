#ruby base image
FROM ruby:3.3.5-slim

# environment variables
ENV RAILS_ENV=development \
    RACK_ENV=development \
    BUNDLE_JOBS=4 \
    BUNDLE_RETRY=3 \
    LANG=C.UTF-8 \
    LC_ALL=C.UTF-8

# dependencies required by Rails, PostgreSQL, Node or Yarn
RUN apt-get update -qq && \
    apt-get install -y \
        build-essential \
        libpq-dev \
        nodejs \
        yarn \
        git \
        vim \
        bash-completion \
        curl \
        default-mysql-client \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY Gemfile Gemfile.lock ./

RUN bundle install

COPY . .

EXPOSE 3000

CMD ["bash", "-c", "rails db:create db:migrate && rails server -b 0.0.0.0"]