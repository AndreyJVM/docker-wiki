| command  | Description |
| ------------- | ------------- |
| `docker version` | Вывод информации о клеите и сервере Docker  |
| `docker ps -a`  | Вывод информации о запущенных и остановленных контейнерах  |
| `docker images` | Вывод списка локальных образов |
| `docker run <container_name>`| Создание контейнера |
| `docker rm <container_name or container_id>`| Удаление контейнера |
| `docker container prune` | Удаляем все остановленные контейнеры |
| `docker rm -f $(docker ps -aq)` | Принудительное удаление всех контейнеров |
| `docker run -it <container_name>`| Переход в интерактивный режим контейнера |
| `docker run -d <container_name>` | Запуск контейнера в фоновом режиме |
| `docker container inspect <container_name or container_id>` | Получение информации о контейнере |
| `docker stop <container_name or container_id> ~ docker kill <container_name or container_id> `| Остановка контейнера |
| `docker exec -it <container_name or container_id> bash` | Подключение к запущенному контейнеру |
| `docker run -d --name <cast_name> <container_name>` | Присвоить контейнеру уникальное имя|
| `docker run -p <external_port>:<container_port> <container_name>` | Меппинг портов |
| `docker run -v <local_path>:<container_path> <container_name>` |  Меппинг томов |
| `docker run --rm <container_name>` | Автоматическое удаление остановленных контейнеров |



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