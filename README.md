| command  | Description |
| ------------- | ------------- |
| `docker version` | Вывод информации о клеите и сервере |
| `docker ps -a`  | Вывод информации о всех контейнерах  |
| `docker images` | Вывод списка образов |
| `docker run <container_name>`| Создание контейнера |
| `docker rm <container_name>`| Удаление контейнера |
| `docker container prune` | Удаляем все остановленные контейнеры |
| `docker rm -f $(docker ps -aq)` | Принудительное удаление |
| `docker run -it <container_name>`| Переход в интерактивный режим |
| `docker run -d <container_name>` | Запуск в фоновом режиме |
| `docker container inspect <container_name>` | Получение информации |
| `docker stop <container_name> ~ docker kill <container_name> `| Остановка контейнера |
| `docker exec -it <container_name> bash` | Подключение к контейнеру |
| `docker run -d --name <cast_name> <container_name>` | Присвоить имя|
| `docker run -p <external_port>:<container_port> <container_name>` | Меппинг портов |
| `docker run -v <local_path>:<container_path> <container_name>` |  Меппинг томов |
| `docker run --rm <container_name>` | Автоматическое удаление |



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