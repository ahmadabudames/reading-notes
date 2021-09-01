#  Django Custom User

### Django Best Practices: Custom User Model

> Setup

- create and navigate into a dedicated directory called accounts for our code

- install Django

- make a new Django project called config

- make a new app accounts

- start the local web server


> Custom User Model

***Creating our initial custom user model requires four steps:***


- update config/settings.py

- create a new CustomUser model

- create new UserCreation and UserChangeForm

- update the admin



# DjangoX


> Pip

$ python3 -m venv djangox
$ source djangox/bin/activate
(djangox) $ pip install -r requirements.txt
(djangox) $ python manage.py migrate
(djangox) $ python manage.py createsuperuser
(djangox) $ python manage.py runserver



> Pipenv

$ pipenv install
$ pipenv shell
(djangox) $ python manage.py migrate
(djangox) $ python manage.py createsuperuser
(djangox) $ python manage.py runserver


> Docker

$ docker build .
$ docker-compose up -d
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser


### Setup



# Run Migrations
(djangox) $ python manage.py migrate

# Create a Superuser
(djangox) $ python manage.py createsuperuser

# Confirm everything is working:
(djangox) $ python manage.py runserver

