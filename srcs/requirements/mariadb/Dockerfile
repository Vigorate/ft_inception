
FROM		debian:buster

#			Installing recquired packages
RUN			apt-get update -y && apt-get upgrade -y
RUN			apt-get install mariadb-server -y

COPY		conf/server.conf /etc/mysql/mariadb.conf.d/server.conf

COPY		conf/setup.sh /setup.sh

ENTRYPOINT	["bash", "setup.sh"]

EXPOSE		3306