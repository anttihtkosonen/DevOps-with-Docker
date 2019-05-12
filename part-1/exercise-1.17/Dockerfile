FROM debian
RUN apt-get update && apt-get install -y python3 python3-pip build-essential libssl-dev libffi-dev python-dev wget curl git vim
RUN python3 -m pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose
RUN curl https://cli-assets.heroku.com/install.sh | sh
CMD ["/bin/bash"]
