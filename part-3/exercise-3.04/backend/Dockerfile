FROM alpine
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000

RUN apk add --no-cache git nodejs npm && \
git init . && \
git remote add -t \* -f origin https://github.com/docker-hy/backend-example-docker && \
git checkout master && \
npm install && \
adduser -D app &&\
chown -fR app /node_modules/

USER app 

CMD npm start

