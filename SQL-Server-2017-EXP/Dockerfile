FROM mcr.microsoft.com/mssql/server:2017-latest-ubuntu

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get -y install tzdata 
RUN ln -fs /usr/share/zoneinfo/Europe/Rome /etc/localtime 
RUN dpkg-reconfigure --frontend noninteractive tzdata