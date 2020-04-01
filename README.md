# Laradoc Setup


### Clone your repo

``` 
git clone yourrepourl
```

### Clone laradoc inside your project
```
git clone https://github.com/Laradock/laradock.git
```

### start development env
```
cd /laradoc

sudo docker-compose up -d nginx mysql php-fpm phpmyadmin

sudo docker-compose ps

sudo docker-compose exec workspace bash

sudo docker-compose restart nginx

sudo docker-compose restart php-fpm
```


### Change php.ini
/home/dev/php/laradock/php-fpm/php7.2.ini

### Change nginx
/home/dev/php/laradock/nginx/nginx.conf

### Billd
```
sudo docker-compose up -d --build nginx mysql
```

### Build without cache
```
sudo docker-compose build --no-cache mysql
```

### Run command within container - within going to bash or container.
``` 
sudo docker exec -it laradock_workspace_1 composer update

sudo docker exec -it laradock_workspace_1 npm run development
```
