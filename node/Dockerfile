FROM node:8.5

RUN useradd --user-group --create-home --shell /bin/false app

ENV HOME=/home/app

COPY package.json $HOME/node/
RUN chown -R app:app $HOME/*

USER app
WORKDIR $HOME/node
RUN npm install
CMD npm start
