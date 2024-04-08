FROM jenkins/jenkins

# install docker, docker-compose, docker-machine
# see: https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/
# see: https://docs.docker.com/engine/installation/linux/linux-postinstall/
# see: https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/


USER root
# RUN echo "deb http://archive.debian.org/debian/ stretch main" > /etc/apt/sources.list \
#     && echo "deb-src http://archive.debian.org/debian/ stretch main" >> /etc/apt/sources.list \
#     && echo "Acquire::Check-Valid-Until false;" > /etc/apt/apt.conf.d/99no-check-valid-until

# RUN apt-get update \
#     && apt-get -y install \
#         apt-transport-https \
#         ca-certificates \
#         curl \
#         software-properties-common





# echo \
# "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
#   $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
# tee /etc/apt/sources.list.d/docker.list > /dev/null



# curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"



echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  tee /etc/apt/sources.list.d/docker.list > /dev/null