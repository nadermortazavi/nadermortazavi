# Pull base image.FROM ubuntu
# update container
FROM ubuntu:latest 
RUN \
apt-get update && \
apt-get install wget -y && \
apt-get install zip -y && \
apt-get install unzip -y && \
# Get sloctl
wget -O sloctl-linux-0.0.56.zip "https://github.com/nobl9/sloctl/raw/main/sloctl-linux-0.0.56.zip" &&\
unzip sloctl-linux-0.0.56.zip -d /usr/local/bin/ && \
rm -rf sloctl-linux-0.0.56.zip && \
chmod a+rx /usr/local/bin/sloctl && \
mkdir -p /.config/nobl9/ && \
chmod 0700 /.config/nobl9/
#COPY config.toml ~/.config/nobl9/config.toml

#
# Define mountable directories.
#VOLUME [/usr/local/bin/]
# Define working directory.
WORKDIR /
# Define default command.
CMD []
# Expose ports.
EXPOSE 80
EXPOSE 443
