FROM ubuntu

RUN apt-get update && apt-get upgrade -y && apt-get install -y vim \
	build-essential git valgrind zsh curl

RUN chsh -s /usr/bin/zsh root && \
	sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" && \
	sed  's/ZSH_THEME/#ZSH_THEME/' ~/.zshrc > ~/.zshrc && \
	echo "ZSH_THEME=\"bira\"" > ~/.zshrc

CMD /usr/bin/zsh
