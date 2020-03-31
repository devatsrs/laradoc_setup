# laradoc_setup
Laradoc Setup


-------------------------
clone your repo
git clone yourrepourl

clone laradoc inside your project
git clone https://github.com/Laradock/laradock.git

cd /laradoc
sudo docker-compose up -d nginx mysql php-fpm phpmyadmin

sudo docker-compose ps
sudo docker-compose exec workspace bash
sudo docker-compose restart nginx
sudo docker-compose restart php-fpm



change php.ini
/home/dev/php/laradock/php-fpm/php7.2.ini

change nginx
/home/dev/php/laradock/nginx/nginx.conf

#billd
sudo docker-compose up -d --build nginx mysql


#build without cache
sudo docker-compose build --no-cache mysql


#run command within container - within going to bash or container.
sudo docker exec -it laradock_workspace_1 composer update

sudo docker exec -it laradock_workspace_1 npm run development
