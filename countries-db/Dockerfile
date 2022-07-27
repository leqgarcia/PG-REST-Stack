FROM postgres:14

RUN apt update -y
RUN apt install python3 python3-pip postgresql-plpython3-11 wget git -y

ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=Sonata!
ENV POSTGRES_DB=postgres

ENV DB_ANON_ROLE=anon
ENV DB_SCHEMA=public

WORKDIR /initdb

RUN cd /initdb

RUN wget https://raw.githubusercontent.com/mattddowney/compose-postgrest/master/initdb/world.sql
RUN wget https://raw.githubusercontent.com/leqgarcia/PG-REST-Stack/main/countries-db/initdb/admin_tasks.sql

ENV PYTHONPATH=/usr/lib/python3.9
