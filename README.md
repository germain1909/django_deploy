Commands for running locally on mac that I used 
Have to be in the same directory as the docker compose file

docker-compose build
docker-compose up -d
docker ps -a //list all running containers
docker-compose run web python3  manage.py migrate


Also have to create databse users manually meaning the postgres user from env file

Command to access postgres database: 
$docker-compose exec postgres psql -U unicorn_user postgres

CREATE USER postgres WITH PASSWORD 'postgres' CREATEDB CREATEROLE LOGIN;
//create a postgres role

CREATE DATABASE [IF NOT EXISTS] db_name;
//create database


Access running site on
http://localhost/catalog/
Which is same as http://localhost:80/catalog/