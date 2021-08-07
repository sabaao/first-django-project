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

# Create a new django app
```
python manage.py startapp blog
```

Add setting in mysite/setting.py
```
INSTALLED_APPS = (
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'blog',
)
```

# Add new blog model
Modify blog/models.py
And run this commit to syncdb.
```
python manage.py makemigrations
python manage.py migrate
```

# Django admin
Modify blog/admin.py
```
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

And run your django server
```
python manage.py runserver
```

# Create django superuser
```
python manage.py createsuperuser
```
# Reference
https://carolhsu.gitbooks.io/django-girls-tutorial-traditional-chiness/content/django_start_project/README.html
https://djangogirlstaipei.gitbooks.io/django-girls-taipei-tutorial/content/django/models.html