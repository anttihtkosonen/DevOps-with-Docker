
FROM node:alpine
ENV LC_ALL=C.UTF-8 
ENV PATH "$PATH:/root/.local/bin"
RUN apk add --no-cache python3 libffi-dev wget curl git vim &&\ 
    apk add --no-cache --virtual .build-deps python3-dev libstdc++ g++ gcc bash\ 
    gfortran python3-dev build-base freetype-dev libpng-dev openblas-dev &&\
    ln -s /usr/include/locale.h /usr/include/xlocale.h &&\
    pip3 install --upgrade pip &&\
    pip3 install --user numpy scipy matplotlib ipython jupyter pandas sympy nose &&\
    curl https://cli-assets.heroku.com/install.sh | bash &&\
    apk del .build-deps &&\
    adduser -D app

USER app
WORKDIR /app 

CMD ["/bin/ash"]
