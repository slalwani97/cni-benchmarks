FROM nginx

COPY ./default.conf /etc/nginx/conf.d/default.conf

RUN mkdir /usr/share/nginx/data

RUN  apt-get update && apt-get install -y wget 

RUN wget http://212.183.159.230/200MB.zip -P /usr/share/nginx/data

# COPY ./200MB.zip /usr/share/nginx/data/200MB.zip

# CMD ["nginx -s reload"]
