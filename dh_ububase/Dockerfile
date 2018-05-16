FROM ubuntu:18.04
LABEL Mantainer="Francisco J. Bejarano <fjbejarano@gmail.com>"
RUN apt-get -y update && apt-get -y dist-upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
    apt-utils \
    vim \
    unzip \
    sudo \
    rsyslog \
    dialog \
    openssh-server \
    apache2 \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

CMD ["/usr/sbin/apache2","-D","FOREGROUND"]
EXPOSE 80