# Install bot

```sh
# run setup
sudo chmod +x ./setup.sh; sudo ./setup.sh

# go to docker & install composer
sudo docker exec -it php /bin/bash
composer install
exit

# Change domains & email ./init-letsencrypt.sh строка 8, 11
mcedit ./init-letsencrypt.sh

# dockers up
sudo docker-compose up -d

# Get ssl sertificate
sudo ./init-letsencrypt.sh

# Migrate DB structure
sudo docker exec -i mariadb mysql -udb_user -pdb_password db_name < ./bot/structure.sql
```
# Docs

## Lets`encrypt
https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71

## PHP telegram bot
https://github.com/php-telegram-bot/core

## API

https://api.telegram.org/


