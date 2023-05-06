# Setting up Static Files

Static files are files that don't change, such as images, CSS, and JavaScript. These files are served directly by your web server and don't require any special processing by Django.

Here's how to set up static files in your Django project:

1. Create a directory called `static` in your project's root directory.

2. Inside the `static` directory, create another directory with the same name as your app. For example, if your app is called `example`, create a directory called `example` inside the `static` directory.

3. Place your static files inside the app's directory. For example, if you have a CSS file called `style.css`, place it inside `static/example/style.css`.

4. In your app's `views.py` file, import the `django.shortcuts.render` function:

``` 
from django.shortcuts import render
```

5. In your view function, add the following line of code to tell Django to serve static files:

``` 
from django.conf import settings

def my_view(request):
context = {}
return render(request, 'my_template.html', context)

if settings.DEBUG:
from django.contrib.staticfiles.urls import staticfiles_urlpatterns
urlpatterns += staticfiles_urlpatterns()
```

Note that the `if settings.DEBUG:` block should only be used in development mode, as it can be a security risk in production.

6. In your project's `urls.py` file, add the following lines of code to tell Django where to find static files:

``` 
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
# Your URL patterns here
]

if settings.DEBUG:
urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
```

Make sure to replace `STATIC_URL` and `STATIC_ROOT` with the appropriate values for your project.

Your static files should now be served correctly by Django.

