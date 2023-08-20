FROM postgres:12.11

# copy the world schema file to 
COPY mydata/world.sql /docker-entrypoint-initdb.d/

# Add htop and curl
RUN apt-get update -y && apt-get install -y htop curl && rm -rf /var/lib/apt/lists/*

# let's create database, username and password environment variables
ENV POSTGRES_DB world
ENV POSTGRES_USER postgres
ENV POSTGRES_PASSWORD postgres

