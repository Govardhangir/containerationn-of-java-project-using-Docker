FROM mysql:8.0.33
ENV MYSQL_ROOT-PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

#ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
ADD db_backup.sql ./db_backup.sql
