FROM alpine as build-stage
EXPOSE 5000

ENV API_URL=http://localhost:8000
WORKDIR frontend

RUN apk add --no-cache nodejs npm git && \
git init . && \
git remote add -t \* -f origin https://github.com/docker-hy/frontend-example-docker && \
git checkout master && \
npm install webpack &&\
npm run build

FROM nginx

COPY --from=build-stage /frontend/dist/ /usr/share/nginx/html

EXPOSE 5000
