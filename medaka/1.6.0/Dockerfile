#######################################################################################################################################################################
# Medaka
#######################################################################################################################################################################

FROM ubuntu
MAINTAINER Sagnik Banerjee <sagnikbanerjee15@gmail.com>
LABEL org.opencontainers.image.source https://github.com/sagnikbanerjee15/dockerized_tools_and_pipelines

ENV TZ=America/New_York
ENV DEBIAN_FRONTEND=noninteractive

#######################################################################################################################################################################
# SETUP
#######################################################################################################################################################################

RUN apt-get -y update
RUN apt-get -y install git python3.8 less vim wget time zlib1g zlib1g-dev lzma-dev \
	libncurses5-dev libcurl4-nss-dev liblzma-dev libncursesw5-dev make unzip zip build-essential \
	gcc g++ cmake ca-certificates libbz2-dev xz-utils htop autoconf automake binutils bison flex \
	gettext libtool make patch pkg-config p7zip-full p7zip python r-base curl sudo python3-pip
RUN sudo apt install default-jre -y
RUN apt-get clean all
RUN pip install numpy
RUN sudo apt-get autoclean autoremove

#######################################################################################################################################################################
# Medaka
#######################################################################################################################################################################

RUN pip install medaka