FROM ubuntu
EXPOSE 3000
RUN apt-get update && apt-get install -y npm nodejs git
RUN git clone https://github.com/anttihtkosonen/full-stack-open-2018/
WORKDIR /full-stack-open-2018/osa2/teht_2.12-2.13
RUN npm install -g npm@latest
RUN rm -rf node_modules
RUN npm install
RUN npm install axios
CMD npm start
