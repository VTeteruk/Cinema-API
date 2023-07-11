# Cinema API

API service for cinema management

## Installing using github

#### Install PostgresSQL and create DB

#### - Using terminal only
```
    git clone https://github.com/VTeteruk/Cinema-API.git
    cd Cinema-API
    python -m venv venv
    sourse venv/bin/activate
    pip install -r requirements.txt
    set SECRET_KEY=your_secret_key
    set POSTGRES_HOST=your_db_host
    set POSTGRES_NAME=your_db_name
    set POSTGRES_USER=db_user
    set PASSWORD=db_password
    python manage.py migrate
    python manage.py runserver
```
#### - Using .env.sample
Firstly
```
    git clone https://github.com/VTeteruk/Cinema-API.git
    cd Cinema-API
    python -m venv venv
    sourse venv/bin/activate
    pip install -r requirements.txt
```
Then inside `.env.sample` write your data and rename the file to `.env`

Finally
```
    python manage.py migrate
    python manage.py runserver
```

## Run with docker
Docker should be installed
```
    docker-compose build
    docker-compose up
```

## Getting access

* create user via /api/user/register
* get access token via api/user/token

## Features
* JWT authenticated
* Admin panel /admin/
* Documentation is located at api/doc/swagger
* Managing movies with genres, actors
* Creating cinema halls
* Adding movie sessions
* Filtering movies and movie sessions
* The ability to add photos to movies 