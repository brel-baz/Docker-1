FROM debian:latest
RUN apt-get update -y
RUN apt-get install -y wget  && apt-get install -y bzip2
RUN apt-get install sudo -y
RUN adduser teamspeak --disabled-login --gecos ""
RUN wget http://dl.4players.de/ts/releases/3.1.0/teamspeak3-server_linux_amd64-3.1.0.tar.bz2
RUN tar -jxf teamspeak3-server_linux_amd64-3.1.0.tar.bz2
RUN rm teamspeak3-server_linux_amd64-3.1.0.tar.bz2
WORKDIR /teamspeak3-server_linux_amd64
RUN echo "license_accepted=1" >> .ts3server_license_accepted
RUN chown -R teamspeak:teamspeak .
CMD sudo -u teamspeak ./ts3server_minimal_runscript.sh
