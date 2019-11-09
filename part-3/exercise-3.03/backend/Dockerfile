FROM ubuntu
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000

RUN apt-get update && apt-get install -y curl nodejs npm git && \
curl -sL https://deb.nodesource.com/setup_10.x | bash && \
git init . && \
git remote add -t \* -f origin https://github.com/docker-hy/backend-example-docker && \
git checkout master && \
npm install && \
apt-get purge -y --auto-remove curl git && \ 
rm -rf /var/lib/apt/lists/* && \ 
useradd -m app &&\
chown -fR app /node_modules/

USER app 

CMD npm start

