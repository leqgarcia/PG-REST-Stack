FROM postgres:14

RUN apt update -y
RUN apt install python3 python3-pip postgresql-plpython3-11 wget git

WORKDIR /initdb

RUN wget https://raw.githubusercontent.com/mattddowney/compose-postgrest/master/initdb/world.sql
RUN wget https://raw.githubusercontent.com/mattddowney/compose-postgrest/master/initdb/create-anon-role.sh

ENV PYTHONPATH=/usr/lib/python3.9
