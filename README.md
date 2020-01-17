Данный репозиторий содержит файлы для выполнения ДЗ.

1. Директория ```nginx``` содержит Dockerfile для создания образа с nginx, конфиг ```nginx.conf``` для подключения php и файл info.php
2. Директория ```php``` содержит Dockerfile для создания образа с php и файл info.php
3. Файл docker-compose.php позволяет запустить два контейнера с образами nginx и php и обеспечить между ними связность.
4. Для проверки ДЗ необходимо выполнить команду ```docker-compose up -d``` и перейти по адресу http://ipnginx/info.php
5. Для проверки, так же, можно перейти по адресу http://34.70.45.123/info.php - там развернут стенд с nginx и php.
6. Образы nginx и php доступны в docker hub по ссылкам: https://hub.docker.com/repository/docker/alexmarychev/nginx и https://hub.docker.com/repository/docker/alexmarychev/php

