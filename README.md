# Homework 2: Docker
## Проверка на сервере

При проверке на environ01:

- Запустить команду ``` export DOCKER_BUILDKIT=1 ``` это нужно для изменения прав bash-файла во втором образе, затем запустить ``` docker-compose up -d ```
- Чтобы посмотреть логи второго контейнера, запустить ``` docker logs service2 ```
- Поскольку до контейнеров снаружи не достучаться, после этого заходим в вебсервер ``` docker exec -it service2 bash ```, и обращаемся к нему из него же, выполняя из инструкции ``` curl 127.0.0.1:8000/ ``` и  ``` curl 127.0.0.1:8000/health ```.
- При необходимости повторения процедуры делаем ``` docker-compose down ```, начинаем с первого пункта без первой команды.

## Замечания

- В репозитории два файла ***data.csv***. При подстановке своих данных следует изменять содержимое ***data/data.csv***. Файл ***./data.csv*** и папка ***.idea*** попали в коммит по недосмотру.