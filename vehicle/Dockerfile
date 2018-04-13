# Virtual-Vehicles Vehicle microservice Dockerfile

FROM java:8u45-jdk
MAINTAINER Gary A. Stafford <garystafford@rochester.rr.com>

ENV REFRESHED_AT 2015-06-15

RUN sed 's/main$/main universe/' -i /etc/apt/sources.list
#RUN apt-get -y update
#RUN apt-get -y upgrade
#RUN apt-get -y dist-upgrade
#RUN apt-get -y clean
#RUN apt-get -y autoclean
#RUN apt-get -y autoremove

COPY ./artifacts /usr/share/java/virtual-vehicles
WORKDIR /usr/share/java/virtual-vehicles

EXPOSE 8581

ENTRYPOINT ["java", "-classpath", ".:config:", "-jar", "Vehicle-1.0-SNAPSHOT.jar", "prod", "com.example.vehicle.Main"]
CMD [""]