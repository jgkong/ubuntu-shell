FROM ubuntu:18.04

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
		command-not-found net-tools vim iputils-ping telnet dnsutils screen curl wget bash-completion \
	&& apt-get clean \
	&& rm -rf /tmp/* /var/tmp/* /var/log/*.log /var/log/apt/*.log \
	&& rm -fr /var/lib/apt/lists/*

CMD ["tail", "-f", "/dev/null"]
