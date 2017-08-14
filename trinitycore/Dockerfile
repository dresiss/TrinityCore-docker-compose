FROM ubuntu:latest
RUN apt-get update && apt-get install -y git build-essential cmake make gcc g++ libmysqlclient-dev libssl-dev libbz2-dev libreadline-dev libncurses-dev libboost-all-dev p7zip
RUN mkdir /trinity/ && cd /trinity/ && git clone git://github.com/TrinityCore/TrinityCore.git
RUN mkdir /trinity/TrinityCore/build/ && cd /trinity/TrinityCore/build/ && cmake ../ -DCMAKE_INSTALL_PREFIX=/wow/server -DTOOLS=0
RUN cd /trinity/TrinityCore/build && make && make install
