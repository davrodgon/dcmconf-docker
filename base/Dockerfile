FROM java:openjdk-8-jre

MAINTAINER David Rodriguez davrodgon@users.sf.net

RUN curl -L -o /tmp/dcmconf-installer.jar https://sourceforge.net/projects/privacyguard/files/latest/download
RUN curl -L -o /tmp/auto-install.xml https://sourceforge.net/projects/privacyguard/files/1.4.6/auto-instal.xml/download

RUN mkdir /opt/dcmconf

RUN java -jar /tmp/dcmconf-installer.jar /tmp/auto-install.xml

RUN rm /tmp/dcmconf-installer.jar /tmp/auto-install.xml


WORKDIR /opt/dcmconf/bin

VOLUME /opt/dcmconf/logs 
VOLUME /opt/dcmconf/data 
VOLUME /opt/dcmconf/etc 


