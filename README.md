# Django-Web-Application-Structure-Best-Practices

myproject/
    manage.py
    myproject/
        __init__.py
        urls.py
        wsgi.py
        settings/
            __init__.py
            base.py
            dev.py
            prod.py
    blog/
        __init__.py
        models.py
        managers.py
        views.py
        urls.py
        templates/
            blog/
                base.html
                list.html
                detail.html
        static/
           …
        tests/
            __init__.py
            test_models.py
            test_managers.py
            test_views.py
    users/
        __init__.py
        models.py
        views.py
        urls.py
        templates/
            users/
                base.html
                list.html
                detail.html
        static/
            …
        tests/
            __init__.py
            test_models.py
            test_views.py
     static/
         css/
             …
         js/
             …
     templates/
         base.html
         index.html
     requirements/
         base.txt
         dev.txt
         test.txt
         prod.txt

The rest of this article explains how to move a project to this layout and why this layout is better.
Current Default Layout

We’re going to call our example project foo, yes I realize it’s a very creative name. We’re assuming here that we’re going to be launching foo.com but while we like to have our project names reflect the ultimate domain(s) the project will live on this isn’t by any means required.

If you kick off your project using django-admin.py startproject foo you get a directory structure like this:

    foo/
        manage.py
        foo/
           __init__.py
           settings.py
           urls.py
           wsgi.py
