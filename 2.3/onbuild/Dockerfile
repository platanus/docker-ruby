FROM platanus/ruby:2.3.1

MAINTAINER Juan Ignacio Donoso "juan.ignacio@platan.us"

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY Gemfile /usr/src/app/Gemfile
ONBUILD COPY Gemfile.lock /usr/src/app/Gemfile.lock

ONBUILD RUN bundle install

ONBUILD COPY . /usr/src/app
