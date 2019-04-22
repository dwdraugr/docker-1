FROM ubuntu

RUN apt-get update && apt-get upgrade -y && apt-get install -y vim \
	build-essential git valgrind zsh curl

WORKDIR /root/

CMD /usr/bin/zsh

# docker run -v ~/:/root/ -it --security-opt seccomp=unconfined envir     