FROM ubuntu
EXPOSE 8000
RUN apt-get update && apt-get install -y curl nodejs npm git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN git clone https://github.com/docker-hy/backend-example-docker
WORKDIR /backend-example-docker/
RUN npm install
CMD npm start
