# Django-tutorial
- take place in [Cloud9](https://c9.io)
- for AskDjango Hackathon

----

### 2017-06-27
- How to run server on c9
```
$ python manage.py runserver $IP:$PORT
```
- Add admin 
    - url: http://django-tutorial-njir.c9users.io/admin/login/?next=/admin/
- Create super user(admin)
```
$ python manage.py createsuperuser
```

### 2017-06-23
- Create Model
```
$ source djangoEnv/bin/activate
$ python manage.py startapp ModelName
```

- Add Post model to DB
```
$ python manage.py makemigrations blog # notice to Django
$ python manage.py migrate blog
```


### 2017-06-22
- Set Virtual environment
```
$ sudo apt-get update
$ sudo apt-get install python3.4-venv
$ python3 -m venv djangoEnv # after that "djangoEnv" folder created
$ source djangoEnv/bin/activate
```

- Install Django
```
$ sudo pip install django~=1.10.0
```

- Create Django project
```
$ source djangoEnv/bin/activate
$ django-admin startproject mysite .
```

> No module named Django Error
```
$ python -m pip install django
```

- Set database and Run server
```
$ python manage.py migrate   # set database
$ python manage.py runserver $IP:$PORT # run server for c9
```
