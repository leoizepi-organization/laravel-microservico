FROM nginx
RUN apt-get update && apt-get install -y wget
#RUN apt-get update && apt-get install -y iputils-ping

WORKDIR /var/www

ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz

RUN rm /etc/nginx/conf.d/default.conf

#COPY ./nginx.conf /etc/nginx/conf.d