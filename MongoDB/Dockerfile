FROM mongo:7.0.12
#FROM mongo:4.4.6

RUN export DEBIAN_FRONTEND=noninteractive
RUN apt update && apt -y install tzdata
RUN ln -fs /usr/share/zoneinfo/Europe/Rome /etc/localtime
RUN dpkg-reconfigure --frontend noninteractive tzdata