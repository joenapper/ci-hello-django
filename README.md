Simple to do list app created using Django full stack framework. Includes complete CRUD functionality

View live site @ https://to-do-app-version1a.herokuapp.com/

-----------------------------

pip3 install django

cd /workspace/.pip-modules/lib/python3.8/site-packages/
^^ python version may vary - while typing python press tab for auto-complete

ls -la
^^ lists all files in directory

cd -
^ back to previous directory

django-admin startproject django_todo .

python3 manage.py runserver

----------------------

python3 manage.py startapp todo

-----------------------------

python3 manage.py makemigrations --dry-run

python3 manage.py showmigrations

python3 manage.py migrate --plan

python3 manage.py migrate

python3 manage.py createsuperuser

-----------------------

python3 manage.py makemigrations --dry-run

python3 manage.py makemigrations

python3 manage.py showmigrations

python3 manage.py migrate --plan

python3 manage.py migrate

--------------------
---------------------

pip3 install coverage

coverage run --source=todo manage.py test

coverage report

coverage html

python3 -m http.server

-----------------
### Deployment

pip3 install psycopg2-binary

pip3 install gunicorn

pip3 freeze --local > requirements.txt

heroku apps:create (name) --region eu

pip3 install dj_database_url

heroku config

python3 manage.py migrate

--------------------

heroku config:set DISABLE_COLLECTSTATIC=1

web: gunicorn django_todo.wsgi:application