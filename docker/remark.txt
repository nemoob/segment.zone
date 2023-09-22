# 基础镜像 centos latest 版本
FROM centos:latest
# 备注作者和邮箱
MAINTAINER yangzhongren "yang_zhong_ren@aliyun.com"

WORKDIR /usr/local/java

ADD jdk-8u351-linux-x64.tar.gz /usr/local/java/
ENV JAVA_HOME=/usr/local/java/jdk1.8.0_351
ENV CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH=$JAVA_HOME/bin:$PATH
