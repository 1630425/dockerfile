FROM chengt/nodejs:latest
MAINTAINER chengt 1630425@qq.com

RUN npm install gitbook-cli -g

RUN apk add --no-cache openssh
RUN ssh-keygen  -t rsa -P '' -f ~/.ssh/id_rsa
RUN git config --global user.email "1630425@qq.com"
RUN git config --global user.name "chengt"

RUN sed -i 's/#   StrictHostKeyChecking no/#   StrictHostKeyChecking no/' /etc/ssh/ssh_config

EXPOSE 4000