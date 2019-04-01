# Purpose
This repo serves as a quickstart for setting up the development/production environment for the Charitree project.

# Usage
1. Clone this repo
```
git clone https://github.com/tobiaslim/docker-compose-charitree-env.git
```

2. For development environment
```
docker-compose up
```

Then setup the codes in the www folder.

3. For production environment

```
docker-compose --file docker-compose-production.yml up --build
```
Then proceed SSH into the container and create a .env file with the following parameters

```
APP_ENV=local
APP_DEBUG=false
APP_KEY=
APP_TIMEZONE=UTC


# Key in your database information here
# Duplicate this file and rename as .env for it to work. 
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=Charitree
DB_USERNAME=root
DB_PASSWORD=tiger

CACHE_DRIVER=file
QUEUE_DRIVER=sync
```