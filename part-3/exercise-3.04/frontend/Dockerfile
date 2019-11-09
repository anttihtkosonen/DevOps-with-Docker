FROM alpine
EXPOSE 5000

ENV API_URL=http://localhost:8000
WORKDIR frontend

RUN apk add --no-cache nodejs npm git && \
git init . && \
git remote add -t \* -f origin https://github.com/docker-hy/frontend-example-docker && \
git checkout master && \
npm install && \
rm -rf /src && \ 
adduser -D app &&\
chown -fR app /frontend/

USER app 


CMD npm start
