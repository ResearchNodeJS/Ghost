FROM ghost:3.40.2
RUN apt-get update -y && \
    # apt-get purge mysql-server && apt-get purge mysql-common && rm -rf /var/log/mysql && rm -rf /var/log/mysql.* && rm -rf /var/lib/mysql && rm -rf /etc/mysql \
    # apt-get install -y mysql-client
	apt-get install -y default-mysql-client --fix-missing --fix-broken #mariadb-client
COPY ./wait-for-it.sh /usr/local/bin/wait-for-it.sh
RUN chmod +x /usr/local/bin/wait-for-it.sh
RUN chmod -R 775 /var/lib/ghost
VOLUME /var/lib/ghost
EXPOSE 80