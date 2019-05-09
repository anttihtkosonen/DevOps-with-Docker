FROM ubuntu
EXPOSE 5000
RUN apt-get update && apt-get install -y curl nodejs npm git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN git clone https://github.com/docker-hy/frontend-example-docker
WORKDIR /frontend-example-docker/
ENV API_URL=http://localhost:8000
RUN npm install
CMD npm start
