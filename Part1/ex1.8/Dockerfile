FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY ./install.sh .

COPY ./echo-web.sh .

RUN chmod +x ./install.sh ./echo-web.sh

RUN ./install.sh

CMD ./echo-web.sh


