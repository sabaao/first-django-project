# first-django-project

# Install Django
```
pip3 install django 
```

# Create a Django project
```
django-admin.py startproject mysite .
```
Then you can see mysite folder.

# How do change timezone
Open mysite/setting.py , and modify variable.
```
USE_TZ = False
TIME_ZONE = 'Asia/Taipei'
```

# Change database destation
If you want use your database, you can change config in setting.py , django default use sqlite3 .

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
```

# Run server
```
python manage.py runserver
```
# Reference
https://carolhsu.gitbooks.io/django-girls-tutorial-traditional-chiness/content/django_start_project/README.html