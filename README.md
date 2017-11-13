# Python: Getting Started

A barebones Django app, which can easily be deployed to Heroku.

This application supports the [Getting Started with Python on Heroku](https://devcenter.heroku.com/articles/getting-started-with-python) article - check it out.

## Running Locally

Make sure you have Python [installed properly](http://install.python-guide.org).  Also, install the [Heroku Toolbelt](https://toolbelt.heroku.com/) and [Postgres](https://devcenter.heroku.com/articles/heroku-postgresql#local-setup).

```sh
$ git clone git@github.com:heroku/python-getting-started.git
$ cd python-getting-started

$ pipenv install

$ createdb python_getting_started

$ python manage.py migrate
$ python manage.py collectstatic

$ heroku local
```

Your app should now be running on [localhost:5000](http://localhost:5000/).

## Deploying to Heroku

```sh
$ heroku create
$ git push heroku master

$ heroku run python manage.py migrate
$ heroku open
```
or

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## info Usefull

heroku login

heroku create <name_app> (sin mayusculas)

heroku ps:scale web=1 (activar el dynos)

heroku config:set DISABLE_COLLECTSTATIC=1 (para desactivar la ruta por defecto que tiene heroku para los archivos estaticos)

git push heroku master (despliega correctamente directamente)

heroku run bash (entras en el servidor de heroku)

heroku run python manage.py migrate

heroku pg:psql ---> conectarse a la bd de datos de postgres, equivalente a ejecutar local un psql

## Documentation

For more information about using Python on Heroku, see these Dev Center articles:

- [Python on Heroku](https://devcenter.heroku.com/categories/python)
