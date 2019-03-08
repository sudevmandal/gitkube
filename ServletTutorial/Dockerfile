FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-8-jdk wget
RUN mkdir /usr/local/tomcat
RUN wget http://www-us.apache.org/dist/tomcat/tomcat-7/v7.0.93/bin/apache-tomcat-7.0.93.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-7.0.93/* /usr/local/tomcat/

COPY ServletTutorial.war /usr/local/tomcat/webapps/
EXPOSE 80
CMD /usr/local/tomcat/bin/catalina.sh run
