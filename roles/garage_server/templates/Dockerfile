# Pull base image
FROM hypriot/rpi-ruby:latest
MAINTAINER Justin Aiken <60tonangel@gmail.com>

RUN apt-get -qq update
RUN apt-get install -y build-essential

ADD {{sinatra_app}}.tar /srv/{{sinatra_app}}
WORKDIR /srv/{{sinatra_app}}
RUN cd /srv/{{sinatra_app}}; bundle install

EXPOSE 4567
CMD ["bundle", "exec", "rackup", "config.ru", "-p", "4567", "-o", "0.0.0.0"]

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
