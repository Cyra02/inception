
FROM debian:bookworm

RUN apt update && apt upgrade -y && apt install -y mariadb-server

COPY 50-server.cnf /etc/mysql/mariadb.conf.d/.
COPY sript.sh .

RUN mkdir /run/mysqld && chmod +x sript.sh
#&& chown mysql:mysql /run/mysqld

CMD ["./sript.sh"]

