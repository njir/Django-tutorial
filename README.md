# Django-tutorial
- take place in [Cloud9](https://c9.io)
- for AskDjango Hackathon

----

### 2017-06-30
- Dynamic data

```python
    posts = Post.objects.filter(published_date__lte=timezone.now()).order_by('published_date')
    return render(request, 'blog/post_list.html', {'posts': posts})
```

- Template

```html
{% for post in posts %}
    <div>
        <p>published: {{ post.published_date }}</p>
        <h1><a href="">{{ post.title }}</a></h1>
        <p>{{ post.text|linebreaksbr }}</p>
    </div>
{% endfor %}
```




### 2017-06-29
- Regex
    - ^: 문자열이 시작할 떄
    - $: 문자열이 끝날 때
    - \d: 숫자
    - (): 패턴의 부분을 저장할 때
- ex) ^post/(\d+)/$
    - ^post/ : url이(오른쪽부터) post/로 시작합니다.
    - (\d+) : 숫자(한 개 이상)가 있습니다. 이 숫자로 조회하고 싶은 게시글을 찾을 수 있어요.
    - / : /뒤에 문자가 있습니다.
    - $ : url 마지막이 /로 끝납니다.


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
