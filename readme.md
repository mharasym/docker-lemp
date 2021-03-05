sudo chown -R $USER:$USER /path/to/app
docker-compose up -d

docker-compose exec app php php-command
docker-compose exec app composer composer-command
or
docker run --rm -v $(pwd):/app php:x.x-cli php php-command
docker run --rm -v $(pwd):/app [composer:x.x || composer:latest] composer-command
docker run -it --rm -v $(pwd):/app/ -w /app [node:x.x || node:latest] npm npm-command