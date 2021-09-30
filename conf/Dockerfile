FROM ubuntu
WORKDIR /opt
RUN apt-get update || true
RUN apt-get -y install nodejs
RUN mkdir /opt/opendialog
WORKDIR /opt/opendialog
COPY filter/ filter
COPY test/ test
COPY *.json .
RUN npx yarn install
RUN npm run e2e