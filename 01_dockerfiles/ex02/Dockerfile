FROM ruby
EXPOSE 3000
WORKDIR /opt/app
RUN apt-get update && apt-get install nodejs -y && gem install rails -v 5.0.2 && \
    rails new server && cd server && bundle && \
    rake db:migrate && rake db:seed
