Bootstrap: docker
From: ubuntu:18.04

%labels
Author "Randall Cab White - rcwhite@stanford.edu"

###########
#%setup
###########
###########

#Downlaod packages
%post
  apt-get -ym update
  apt-get -ym install libsdl2-image-2.0-0 libsdl2-image-dev gcc yasm \
wget curl gnupg2 jq sed gawk util-linux libsdl-dev \
git cmake build-essential parallel libjpeg-dev libsdl-image* \
rsync perl ssh openssl coreutils emscripten libpng-dev

#grabbing building libbpg
mkdir /bpgbuild
cd /bpgbuild
git clone https://github.com/mirrorer/libbpg

####
cd libbpg
make
make install
make clean

%environment
  export IMAGE_NAME="libbpg_container"
%runscript
#


