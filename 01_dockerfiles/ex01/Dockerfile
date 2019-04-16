FROM debian

ENV teamspeak_url https://files.teamspeak-services.com/releases/server/3.7.1/teamspeak3-server_linux_amd64-3.7.1.tar.bz2
ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011

RUN apt-get update && apt-get upgrade -y && apt-get install -y curl && \
	apt-get install -y bzip2 && \
	curl -o tp.tar.bz2 $teamspeak_url && \
	tar -xvf tp.tar.bz2

WORKDIR /teamspeak3-server_linux_amd64
RUN touch .ts3server_license_accepted

ENTRYPOINT ["bash", "ts3server_minimal_runscript.sh"]
