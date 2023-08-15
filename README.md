# Настройка compose-файла для работы с MySQL и phpMyAdmin


Перед началом работы с docker-compose была установлена Ubuntu 20.04 Server на VirtualBox.
Далее выполнить следующие шаги:

1. Установить docker ( https://docs.docker.com/engine/install/ubuntu/ )

```shell
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```
2. Проверить, запустился ли докер:

```shell
service docker status
```
3. Установить docker-compose (https://docs.docker.com/compose/install/linux/)

```shell
sudo apt-get update
sudo apt-get install docker-compose-plugin
```
4. Проверить, что docker-compose установился:

```shell
docker compose version
```
5. Настроить окружение для compose-файла. Выполнить команды:
   
```shell
sudo mkdir /opt/compose
cd /opt/compose
sudo mkdir database
sudo touch docker-compose.yml
sudo touch .env
```
6. В файл  [.env](https://github.com/Maryana101/test_compose/blob/main/.env) прописать параметры окружения. В файл docker-compose.yml - содержимое файла [docker-compose.yml](https://github.com/Maryana101/test_compose/blob/c99195216af6cc0446c39db577cbe87c737715a7/docker-compose.yml)

7. Выполнить команду поднятия контейнеров:

```shell
sudo docker compose up -d
```
8. Проверить, что контейнеры запущены:
```shell
docker ps
```
В результате должно быть запущено 2 контейнера:

![изображение](https://github.com/Maryana101/test_compose/assets/103298913/b73742bf-814b-4b39-b397-e26c69c06222)

Также должен открываться phpMyAdmin:

![изображение](https://github.com/Maryana101/test_compose/assets/103298913/2c646027-b2e0-4183-8b4b-d7015abc28ea)

![изображение](https://github.com/Maryana101/test_compose/assets/103298913/f9166a23-a85b-42c3-b210-fc27a90e2d40)


   
