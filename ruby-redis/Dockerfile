FROM ruby:2.2.0

# change timezone
RUN cp /usr/share/zoneinfo/Europe/Istanbul /etc/localtime

# set locale
ENV LANG C.UTF-8

# update the system and install the packages
RUN apt-get update && apt-get install -y build-essential

# for working directory
RUN mkdir /app
WORKDIR /app
ADD Gemfile /app/Gemfile
RUN bundle install
ADD . /app
