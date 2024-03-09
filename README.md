# kittygram
## Описание
#### Яндекс Практикум
#### Спринт 16

### Проект kittygram позволяет пользователям выкладывать анкеты котов, а также просматривать анкеты, выложенные другими пользователями. В анкете можно загрузить фотографию, указать имя, год рождения, выбрать цвет и указать достижения вашего питомца.


### Как запустить проект:

#### Форкнуть репозиторий.
#### Клонировать форкнутый репозиторий и перейти в него в командной строке:

##### git clone https://github.com/***username***/kittygram_final.git
##### cd kittygram_final

#### После приготовлений, описанных ниже, пушим приложение на github:
```
git add .
git commit -m 'my commit'
git push
```
##### Проект пройдёт тесты и запустится на сервере

### Как подготовить сервер:
```
На сервере, где разворачивается проект, должен быть установлен Docker
```
#### Установка докера:
##### Windows: установите WSL [по инструкции](https://learn.microsoft.com/ru-ru/windows/wsl/install), после чего установите [Docker Desktop](https://www.docker.com/products/docker-desktop/).
##### macOS: установите [Docker Desktop](https://www.docker.com/products/docker-desktop/)
##### Linux: установите Docker Engine, используя готовый скрипт от Docker:
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
```
#### Создаём директорию проекта на сервере:
```
mkdir ~/kittygram
```
#### Создаём пустой файл .env:
```
touch ~/kittygram/.env
```
### Необходимые переменные окружения:
#### В проекте kittygram переменные окружения передаются на сервер из форкнутого репозитория на github.
#### В окне Actions secrets and variables (https://github.com/***username***/kittygram_final/settings/secrets/actions) необходимо создать следующие секреты:
```
ALLOWED_HOSTS: список хостов/доменов. Писать через запятую, без пробелов
DB_HOST: имя контейнера, где запущен сервер БД
DB_PORT: порт, по которому Django будет обращаться к базе данных
DOCKER_PASSWORD: пароль от вашего докер аккаунта
DOCKER_USERNAME: username вашего докер аккаунта
HOST: IP-адрес вашего сервера
POSTGRES_DB: название БД
POSTGRES_PASSWORD: пароль от БД
POSTGRES_USER: логин БД
SSH_KEY: содержимое закрытого ключа SSH для доступа к серверу
SSH_PASSPHRASE: passphrase для доступа к серверу
TELEGRAM_TO: ID вашего телеграм-аккаунта
TELEGRAM_TOKEN: токен вашего телеграм-бота
USER: ваше имя пользователя на сервере
```

### Использованные технологии:
```
Django
docker
git
PostgreSQL
python
pytest
```
**_Контактная информация_**
Автор проекта:

Алексей Сухоруков
https://github.com/AlekseySuhorukov
eMail: aleksey.suhorukov2@gmail.com
