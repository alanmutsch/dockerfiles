# Run Rainbowstream in a container
#
# docker run -it --rm \
#   -v /etc/localtime:/etc/localtime:ro \
#   -v $HOME/.rainbow_oauth:/root/.rainbow_oauth \ # mount config files
#   -v $HOME/.rainbow_config.json:/root/.rainbow_config.json \
#   --name rainbowstream \

FROM ubuntu:16.04
LABEL maintainer "Alan Mutschelknaus alanmutsch@gmail.com"

RUN apt-get update && apt-get install -y \
        python \
        python-pip \
	ca-certificates 

RUN USER=root pip install \
	 pillow==2.8.0 \
	 rainbowstream

ENTRYPOINT [ "rainbowstream" ]
