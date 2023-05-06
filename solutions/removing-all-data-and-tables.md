# Removing all data and files form an existing Django project

For removing all stored data files, migrations and super user creation
from a django process please follow this steps :


1. Delete all migration files from each app in your project's `migrations` directory, except for the `__init__.py` file. You can use the following command to delete all migration files:

   ```
   find . -path "*/migrations/*.py" -not -name "__init__.py" -delete
   ```

   This command will delete all migration files except for `__init__.py` files in all directories named `migrations` within the current directory and its subdirectories.

2. Delete the contents of the `django_migrations` table in your project's database. You can do this using the following command:

   ```
   python3 manage.py sqlflush | python manage.py dbshell
   ```

   This command will generate the SQL statements needed to truncate all tables in your project's database, including the `django_migrations` table. It will then execute the SQL statements using `dbshell`.

   Alternatively, you can use a tool like `pgAdmin` or `phpMyAdmin` to manually truncate the `django_migrations` table.

3. Delete all tables in your project's database. You can do this using the following command:

``` 
python3 manage.py flush --noinput
```

Now you are left with un-applied migrations and tables.
