FROM ubuntu
RUN apt-get update && apt-get install -y curl
COPY script.sh .
RUN chmod a+x script.sh
RUN ["./script.sh"]
