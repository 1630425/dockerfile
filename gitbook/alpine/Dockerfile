FROM chengt/nodejs:latest
MAINTAINER chengt 1630425@qq.com

RUN npm install gitbook-cli -g
RUN mkdir -p ~/gitbooks/gh-pages
RUN cd ~/gitbooks/gh-pages && git clone https://github.com/1630425/gitbook-documentation.git
RUN rm -rf ~/gitbooks/gh-pages/gitbook-documentation/*

EXPOSE 4000