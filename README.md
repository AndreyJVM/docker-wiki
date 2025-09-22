| command  | Description |
| ------------- | ------------- |
| **docker version** | Вывод информации о клеите и сервере |
| **docker ps -a** | Вывод информации о всех контейнерах  |
| **docker images** | Вывод списка образов |
| **docker run <name>** | Создание контейнера |
| **docker rm <name>** | Удаление контейнера |
| **docker container prune** | Удаляем все остановленные контейнеры |
| **docker rm -f $(docker ps -aq)** | Принудительное удаление |
| **docker run -it <name>** | Переход в интерактивный режим |
| **docker run -d <name>** | Запуск в фоновом режиме |
| **docker container inspect <name>** | Получение информации |
| **docker stop <name> ~ docker kill <name>** | Остановка контейнера |
| **docker exec -it <name> bash** | Подключение к контейнеру |
| **docker run -d --name <cast_name> <name>** | Присвоить имя|
| **docker run -p <external_port>:<container_port> <name>** | Меппинг портов |
| **docker run -v <local_path>:<container_path> <name>** |  Меппинг томов |
| **docker run --rm <name>** | Автоматическое удаление |



### Перенос строк при написании длинных команд
```shell
docker run \
  --name my_nginx \
  -v ${PWD}:/home \
  -p 8080:80 \
  -d \
  --rm \
  nginx
```