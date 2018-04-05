db-on-docker


#Run services
mkdir ~/projs
cd ~/projs
git clone https://github.com/devteds/e8-db-on-docker.git db-on-docker
cd db-on-docker
mkdir data
docker-compose up

# on new terminal tab
cd ~/projs/db-on-docker
docker-compose ps
Test connection - multiple options
Test connection w/ database client on host OS using host OS ports
Test with PHP based adminer tool that run on container - http://localhost:8080

# Test with databse clients within running containers. Examples below

* docker-compose exec mysql-dev mysql -uroot -ppassword blogapp
* docker-compose exec mysql-legacy mysql -uroot -ppassword legacyapp
* docker-compose exec pgdb psql -U root -W blogapp

#A few useful commands
docker-compose stop
docker-compose rm
docker-compose rm -f 