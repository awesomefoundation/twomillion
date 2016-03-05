FROM ruby
MAINTAINER graham@grahamc.com

RUN apt-get update \
 && apt-get install -y node python-pygments

RUN gem install --no-ri --no-rdoc bundler \
 && gem install jekyll rdiscount kramdown jekyll-redirect-from

VOLUME /usr/src/app
EXPOSE 4000

WORKDIR /usr/src/app

COPY ./run.sh /run.sh

CMD ["/run.sh"]