# Django Admin site not showing changes

If you are experiencing issues with Django Admin site not showing changes, there are a few things you can try to resolve the issue:

1. Clear your browser's cache: Sometimes, changes made to your Django project may not be reflected in the Admin site due to caching issues. Clear your browser's cache and try accessing the Admin site again.

2. Check your Django project's `INSTALLED_APPS` setting: Make sure that the app containing the changes you made is included in the `INSTALLED_APPS` setting in your Django project's `settings.py` file. If it is not, add it and try accessing the Admin site again.

3. Check your Django project's `urls.py` file: Make sure that the app containing the changes you made is included in the `urlpatterns` list in your Django project's `urls.py` file. If it is not, add it and try accessing the Admin site again.

4. Register the models in your app's `example.admin.py` file and make suer all the models you want to get in admin panel are registered here.

5. Restart your Django development server: Sometimes, changes made to your Django project may not be reflected in the Admin site due to issues with the development server. Try restarting your Django development server and accessing the Admin site again.

If none of these steps resolve the issue, try searching for solutions online or asking for help in a community forum or discussion board.
