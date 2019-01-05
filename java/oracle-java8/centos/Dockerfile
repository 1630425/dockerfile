FROM registry.cn-hangzhou.aliyuncs.com/centos-7-2_1511/base

MAINTAINER chengt "1630425@qq.com"

ENV JDK_URL http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz
ENV JDK_VERSION 1.8.0_131
ENV TMP_PATH /tmp/src
ENV BUILD_PATH /opt/java

RUN mkdir -v $TMP_PATH $BUILD_PATH \
&& wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" -c $JDK_URL -P $TMP_PATH \
&& tar -xzvf $TMP_PATH/${JDK_URL##*/} -C $BUILD_PATH \
&& ln -s $BUILD_PATH/jdk$JDK_VERSION $BUILD_PATH/java-latest \
&& rm -rf $TMP_PATH

ENV JAVA_HOME $BUILD_PATH/java-latest
ENV CLASSPATH .:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH $PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin

CMD ["/bin/bash"]