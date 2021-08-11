# cbr_rates_docker

1. Установить Docker
2. Склонировать репозиторий в рабочую директорию
```bash
git clone https://github.com/flintpnz/cbr_rates_docker.git
```
3. В docker-compose.yml вписать свои данные для БД MySQL (строки 29-32)
```bash
- MYSQL_ROOT_PASSWORD=
- MYSQL_DATABASE=
- MYSQL_USER=
- MYSQL_PASSWORD=
```
4. В docker-compose.yml по желанию изменить порт 35000 на желаемый (строка 16)
```bash
- '35000:80'
```
5. Склонировать репозиторий Symfony в директорию cbr_rates_docker
```bash
cd cbr_rates_docker
git clone https://github.com/flintpnz/cbr_rates.git
```
6. Запустить сборку контейнеров
```bash
docker-compose up -d
```
7. Добавить в локальный файл hosts выбранный домен
```bash
127.0.0.1 domain.local
```
8. Открыть в браузере http://domain.local:35000