FROM mysql

# Environment variables
ENV MYSQL_ROOT_PASSWORD root
ENV MYSQL_DATABASE test


# Create Database
RUN	mkdir /usr/sql
RUN	chmod a+rx /usr/sql

#ADD ["sql/initial.sql", "/docker-entrypoint-initdb.d/initial.sql"]
ADD ["sql/createTable.sql", "/docker-entrypoint-initdb.d/createTable.sql"]
ADD ["sql/loadData.sql", "/docker-entrypoint-initdb.d/loadData.sql"]

ADD ["BANKDIRECTORYPLUS_V3_FULL_20171027.csv", "/usr/sql/data/data.csv"]


#RUN ["./entrypoint.sh", "mysqld"]






