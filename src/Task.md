
---

## 📄 index.html

Простая HTML-страница, которая отображается в браузере.

```html
<h1>Hello from Erbol</h1>
```
Docker-образ собран на базе nginx:alpine.
HTML-файл копируется в стандартный web-root nginx.

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html


## Сборка Docker-образа

docker build -t my-web-app:latest .


## Скриншот результата сборки образа:

# docker build ...
# (сохранить скриншот и добавить ниже)
![Docker build](./pics/Создание_образа.jpeg)


## Запуск контейнер (через docker run)

![Docker run](./pics/Запуск_контейнера.jpeg)

## Приложение доступно по адресу:


http://localhost:8080


![Browser](./pics/Доступен_8080.jpeg)


## Docker Compose

Для запуска сервиса используется docker-compose.yml.


version: "3.9"

services:
  web:
    image: my-web-app:latest
    ports:
      - "8080:80"


Запуск:

docker compose up -d


Скриншот работающего сервиса:

![Docker Compose](./pics/docker_compose.jpeg
