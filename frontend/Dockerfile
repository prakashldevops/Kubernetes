#This is docker file for myapp Microservices frontend
FROM centos:7
MAINTAINER prakashlavd@gmail.com
RUN yum -y update
ADD config /opt
RUN yum -y install `cat /opt/packages`
ADD code /var/www/html
ENV BACKENDLB=test 
EXPOSE 80
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/start-apache.sh
ENTRYPOINT ["start-apache.sh"]
