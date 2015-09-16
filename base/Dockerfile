FROM java:8-jre

MAINTAINER David Rodriguez davrodgon@users.sf.net

RUN curl -L -o /tmp/installer.jar http://sourceforge.net/projects/privacyguard/files/1.4.4/dcmconf-installer-1.4.4-2.jar/download
RUN curl -L -o /tmp/auto-install.xml http://sourceforge.net/projects/privacyguard/files/1.4.4/dcmconf-auto-install.xml/download

ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64 

RUN java -jar /tmp/installer.jar /tmp/auto-install.xml 

RUN rm /tmp/installer.jar /tmp/auto-install.xml

WORKDIR /opt/dcmconf/bin

VOLUME /opt/dcmconf/logs 
VOLUME /opt/dcmconf/data 
VOLUME /opt/dcmconf/etc 


