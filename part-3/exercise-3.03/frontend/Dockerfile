FROM ubuntu
EXPOSE 5000

ENV API_URL=http://localhost:8000
WORKDIR frontend

RUN apt-get update && apt-get install -y curl nodejs npm git && \
curl -sL https://deb.nodesource.com/setup_10.x | bash && \
git init . && \
git remote add -t \* -f origin https://github.com/docker-hy/frontend-example-docker && \
git checkout master && \
npm install && \
apt-get purge -y --auto-remove curl git && \ 
rm -rf /var/lib/apt/lists/* && \
rm -rf /src && \ 
useradd -m app &&\
chown -fR app /frontend/

USER app 


CMD npm start
