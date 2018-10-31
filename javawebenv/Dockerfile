FROM centos:7
MAINTAINER "378874895@qq.com"
ADD jdk-11.0.1_linux-x64_bin.tar.gz /opt/java
ENV JAVA_HOME /opt/java/jdk-11.0.1
ENV PATH $JAVA_HOME/bin:$PATH
ADD apache-tomcat-9.0.12.tar.gz /opt/tomcat
RUN chmod +x /opt/tomcat/apache-tomcat-9.0.12/bin/*.sh
EXPOSE 8080
ENTRYPOINT /opt/tomcat/apache-tomcat-9.0.12/bin/startup.sh && /bin/bash
