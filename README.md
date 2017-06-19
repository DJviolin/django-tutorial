# Django Official Tutorial

https://lnx.azurewebsites.net/python-dev-environment-with-visual-studio-code-on-linux/

Init:

```
$ cd D:/www/python/django/tutorial
$ .\env\Scripts\activate
$ pip install pep8 pylint pylint_django setuptools
$ code-insiders .
```

##### Upgrading pip

https://pip.pypa.io/en/latest/installing/#installing-with-get-pip-py

On Linux or macOS:

```
$ pip install -U pip
```

On Windows [5]:

```
$ python -m pip install -U pip
```

##### Creating virtual environment

https://docs.djangoproject.com/en/1.11/intro/contributing/

Python 3:

```
$ python -m venv ./env
```

##### Activating virtualenv

```
$ .\env\Scripts\activate
```

##### De-activating virtualenv

```
$ .\env\Scripts\deactivate
```

##### Installing Django

```
pip install -e git+https://github.com/django/django.git@master#egg=django
```

##### Updating Python inside venv

```
$ python -m venv --upgrade ./env
```

##### Updating Django

```
$ cd env/src/django
$ git pull
```

##### Verifying Django Install

```
$ python
>>> import django
>>> print(django.get_version())
```

or:

```
$ python -m django --version
```

##### Accessing Django shell

```
$ python manage.py shell
```

##### Bootstrapping your Django Project

```
$ django-admin startproject mysite .
```

##### Start the development server

```
$ python manage.py runserver 0:8000
```

##### Create the application

```
$ python manage.py startapp polls
```

##### Creating the tables

```
$ python manage.py migrate
```

##### When Django knows to include the polls app

```
$ python manage.py makemigrations polls
```

By running makemigrations, you’re telling Django that you’ve made some changes to your models (in this case, you’ve made new ones) and that you’d like the changes to be stored as a migration.

##### let’s see what SQL that migration would run

```
$ python manage.py sqlmigrate polls 0001
```

##### Now, run migrate again to create those model tables in your database:

```
$ python manage.py migrate
```

##### Run after every model change

```
$ python manage.py makemigrations
$ python manage.py migrate
```

##### Creating an admin user

```
$ python manage.py createsuperuser
```

##### Performing tests

```
$ python manage.py test polls
```
