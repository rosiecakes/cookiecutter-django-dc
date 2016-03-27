cookiecutter-django
===================

[![Requirements Status](https://requires.io/github/pydanny/cookiecutter-django/requirements.svg?branch=master)](https://requires.io/github/pydanny/cookiecutter-django/requirements/?branch=master)

[![Build Status](https://travis-ci.org/pydanny/cookiecutter-django.svg?branch=master)](https://travis-ci.org/pydanny/cookiecutter-django?branch=master)

[![image](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/pydanny/cookiecutter-django?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A [Cookiecutter](https://github.com/audreyr/cookiecutter) template for
Django.

Features
--------

-   For Django 1.9
-   Renders Django projects with 100% starting test coverage
-   Twitter [Bootstrap](https://github.com/twbs/bootstrap) v4.0.0 -
    [alpha](http://blog.getbootstrap.com/2015/08/19/bootstrap-4-alpha/)
-   End-to-end via [Hitch](https://github.com/hitchtest/hitchtest)
-   [AngularJS](https://github.com/angular/angular.js)
-   [12-Factor](http://12factor.net/) based settings via
    [django-environ](https://github.com/joke2k/django-environ)
-   Optimized development and production settings
-   Registration via
    [django-allauth](https://github.com/pennersr/django-allauth)
-   Comes with custom user model ready to go.
-   Grunt build for compass and livereload
-   Basic e-mail configurations for sending emails via
    [Mailgun](https://mailgun.com/)
-   Media storage using Amazon S3
-   Docker support using
    [docker-compose](https://www.github.com/docker/compose) for
    development and production
-   [Procfile](https://devcenter.heroku.com/articles/procfile) for
    deploying to Heroku
-   Works with Python 2.7.x or 3.5.x!
-   Run tests with unittest or py.test!

Optional Integrations
---------------------

*These features can be enabled during initial project setup.*

-   Serve static files from Amazon S3 or
    [Whitenoise](https://whitenoise.readthedocs.org/)
-   Configuration for [Celery](http://www.celeryproject.org/)
-   Integration with [MailHog](https://github.com/mailhog/MailHog) for
    local email testing
-   Integration with [Sentry](https://getsentry.com) for error logging
-   Integration with [NewRelic](https://newrelic.com) for performance
    monitoring
-   Integration with [Opbeat](https://opbeat.com/) for performance
    monitoring

Constraints
-----------

-   Only maintained 3rd party libraries are used.
-   PostgreSQL everywhere (9.0+)
-   Environment variables for configuration (This won't work
    with Apache/mod\_wsgi).

Usage
-----

Let's pretend you want to create a Django project called "redditclone".
Rather than using startproject and then editing the results to include
your name, email, and various configuration issues that always get
forgotten until the worst possible moment, get
[cookiecutter](https://github.com/audreyr/cookiecutter) to do all the
work.

First, get cookiecutter. Trust me, it's awesome:

    $ pip install cookiecutter

Now run it against this repo:

    $ cookiecutter https://github.com/pydanny/cookiecutter-django.git

You'll be prompted for some questions, answer them, then it will create
a Django project for you.

**Warning**: After this point, change 'Daniel Greenfeld', 'pydanny', etc
to your own information.

**Warning**: repo\_name must be a valid Python module name or you will
have issues on imports.

It prompts you for questions. Answer them:

    Cloning into 'cookiecutter-django'...
    remote: Counting objects: 550, done.
    remote: Compressing objects: 100% (310/310), done.
    remote: Total 550 (delta 283), reused 479 (delta 222)
    Receiving objects: 100% (550/550), 127.66 KiB | 58 KiB/s, done.
    Resolving deltas: 100% (283/283), done.
    project_name [project_name]: Reddit Clone
    repo_name [Reddit_Clone]: reddit
    author_name [Your Name]: Daniel Greenfeld
    email [Your email]: pydanny@gmail.com
    description [A short description of the project.]: A reddit clone.
    domain_name [example.com]: myreddit.com
    version [0.1.0]: 0.0.1
    timezone [UTC]:
    now [2016/03/01]: 2016/03/05
    year [2015]:
    use_whitenoise [y]: n
    use_celery [n]: y
    use_mailhog [n]: n
    use_sentry [n]: y
    use_newrelic [n]: y
    use_opbeat [n]: y
    windows [n]: n
    use_python2 [n]: y
    Select open_source_license:
    1 - MIT
    2 - BSD
    3 - Not open source
    Choose from 1, 2, 3 [1]: 1

Enter the project and take a look around:

    $ cd reddit/
    $ ls

Create a GitHub repo and push it there:

    $ git init
    $ git add .
    $ git commit -m "first awesome commit"
    $ git remote add origin git@github.com:pydanny/redditclone.git
    $ git push -u origin master

Now take a look at your repo. Don't forget to carefully look at the
generated README. Awesome, right?

For development, see the following for local development:

-   [Developing
    locally](http://cookiecutter-django.readthedocs.org/en/latest/developing-locally.html)
-   [Developing locally using
    docker](http://cookiecutter-django.readthedocs.org/en/latest/developing-locally-docker.html)

Articles
--------

-   [Development and Deployment of Cookiecutter-Django via
    Docker](https://realpython.com/blog/python/development-and-deployment-of-cookiecutter-django-via-docker)
-   [Development and Deployment of Cookiecutter-Django on
    Fedora](https://realpython.com/blog/python/development-and-deployment-of-cookiecutter-django-on-fedora/)

Support This Project
--------------------

This project is maintained by volunteers. Support their efforts by
spreading the word about:

[![Two Scoops Academy](https://s3.amazonaws.com/tsacademy/images/tsa-logo-250x60-transparent-01.png)](http://www.twoscoops.academy/)

For Readers of Two Scoops of Django 1.8
---------------------------------------

You may notice that some elements of this project do not exactly match
what we describe in chapter 3. The reason for that is this project,
amongst other things, serves as a test bed for trying out new ideas and
concepts. Sometimes they work, sometimes they don't, but the end result
is that it won't necessarily match precisely what is described in the
book I co-authored.

"Your Stuff"
------------

Scattered throughout the Python and HTML of this project are places
marked with "your stuff". This is where third-party libraries are to be
integrated with your project.

Releases
--------

Want a stable release? You can find them at
<https://github.com/pydanny/cookiecutter-django/releases>

Not Exactly What You Want?
--------------------------

This is what I want. *It might not be what you want.* Don't worry, you
have options:

### Fork This

If you have differences in your preferred setup, I encourage you to fork
this to create your own version. Once you have your fork working, let me
know and I'll add it to a '*Similar Cookiecutter Templates*' list here.
It's up to you whether or not to rename your fork.

If you do rename your fork, I encourage you to submit it to the
following places:

-   [cookiecutter](https://github.com/audreyr/cookiecutter) so it gets
    listed in the README as a template.
-   The cookiecutter
    [grid](https://www.djangopackages.com/grids/g/cookiecutters/) on
    Django Packages.

### Or Submit a Pull Request

I also accept pull requests on this, if they're small, atomic, and if
they make my own project development experience better.
