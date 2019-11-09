FROM debian
ENV LC_ALL=C.UTF-8    

RUN apt-get update && apt-get install -y ffmpeg python3 python3-pip rtmpdump \
php7.0 php7.0-bcmath php7.0-curl php7.0-mcrypt php7.0-xml && \
pip3 install -U yle-dl 

WORKDIR /video
ENTRYPOINT ["yle-dl"]

