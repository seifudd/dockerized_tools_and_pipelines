#######################################################################################################################################################################
# pbaa
#######################################################################################################################################################################

FROM conda/miniconda3
MAINTAINER Sagnik Banerjee <sagnikbanerjee15@gmail.com>
LABEL org.opencontainers.image.source https://github.com/sagnikbanerjee15/dockerized_tools_and_pipelines

ENV TZ=America/New_York
ENV DEBIAN_FRONTEND=noninteractive

#######################################################################################################################################################################
# SETUP
#######################################################################################################################################################################

RUN apt-get update && apt-get install -y lsb-release software-properties-common && apt-get clean all
RUN add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) main universe" && \
	apt-get --quiet install --yes zip unzip gcc rsync sudo htop vim less locales locales-all perl python3 rsync zip \
		libidn11 fuse wget curl make zlib1g-dev libffi-dev libncurses5-dev libcurl4-gnutls-dev libssl-dev cmake python3-all-dev && \
	apt-get clean

RUN echo deb http://deb.debian.org/debian/ stretch main >> /etc/apt/sources.list
RUN apt-get install -y libz-dev ncurses-dev liblzma-dev libbz2-dev libcurl4-openssl-dev


#######################################################################################################################################################################
# PBAA - for PacBio data analysis
#######################################################################################################################################################################

RUN conda install -c bioconda pbaa