FROM ubuntu:latest

CMD [ "echo","Hello World" ]

WORKDIR /app 
 
RUN apt-get update && \
    aptget install vim -y

COPY html /usr/share/nginx