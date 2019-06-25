FROM ubuntu

RUN apt update && apt install -y openssh-client && apt install -y openssh-server

RUN printf 'sumit\nsumit\nSumit\n\n\n\n\nY\n' | adduser sumit

WORKDIR /home/sumit

RUN wget http://212.183.159.230/200MB.zip -P /home/sumit

# COPY --chown=sumit:sumit ./200MB.zip /home/sumit/

EXPOSE 22

