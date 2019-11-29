# Setup

1. create new rails project

```
docker-compose run web rails new . --force --no-deps --database=mysql --skip-test --webpacker
```

2. edit `config/database.yml`
※ password is written in docker-compose.yml

```yml
default: &default
  ...
  password: password #here
  host: db # here
```

3. setup

```sh
docker-compose run web rails db:create
docker-compose up
```