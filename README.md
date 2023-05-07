# Django_Tutor

This project is a collection of problems encountered while working with 
Django and their solutions. Each problem has a corresponding solution 
documented in a separate `.md` file. 
The purpose of this project is to serve as a reference for me
and other developers who may be experiencing similar issues.



**_This is not any kind of tutorial or work through.
It's basically solves some issues which includes some boiler code and settings._**

## Table of Contents

- [Problem 1: Django CSRF Verification Failed](./solutions/csrf-verification-failed.md)
- [Problem 2: Django Admin Site Not Showing Changes](./solutions/admin-site-not-showing-changes.md)
- [Problem 3: Django Model Not Saving Data to Database](./solutions/model-not-saving-data.md)
- [Problem 4: Django Static Files Setup](./solutions/static-files-setup.md)
- [Problem 5: Removing all data and tables](./solutions/removing-all-data-and-tables.md)
- [Problem 6: Data-backup-and-restore](solutions/data-backup-and-restore.md)


## Creation and running of a basic Django project

Let's create a basic django project named "django_tutor", and an app called example_app

1. Creating a directory Django

    ```
    mkdir django_tutor
    cd django_tutor
    ```

2. Creating a virtual environment
    - if python virtual environment creating package is not installed the use :
        ```
        python3 -m pip install virtualenv
        ```
    - create the virtual env
        ``` 
        python3 -m venv venv
        ```
      
3. Activate the virtual environment
    - Linux :
        ``` 
        source env/bin/activate
        ```
    - Windows :
        ``` 
        .\env\Scripts\activate
        ```
      
4. Download required packages in the environment
    - django
    - pillow (for handling image files) etc.


5. Create the Django project and the app
    ```
    django-admin startproject djnago_tutor .
    django-admin startapp example_app
    ```
   **The dot at the last denotes that the django project 
   will not create any other directory. 
   And it will use the current directory for project creation.**
   

6. Start the project 
    ``` 
    pyhton3  manage.py runserver
    ```
    This will start a local host server at port 8000 form here you can
    access the website and basically every thing.
      If successful you will see an output of :
   
      ![Django Landing Page](images/django-landing-page.png?raw=true "Django Landing Page")


## Contributing

Contributions to this project are welcome. If you have encountered a problem while working with Django and have found a solution, please feel free to create a pull request with your solution added to the appropriate `.md` file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
