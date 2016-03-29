cookiecutter-django-dc
======================

A Cookiecutter template for Django, for projects disconnected from the regular
internet...

Features like links within READMEs, external APIs and integration (S3, MailHog,
  Sentry, NewRelic, etc) have been disabled.

Set up to use the following pipeline:
- Atlassian Bitbucket
- Concourse CI
- Docker

Features
--------

-   For Django 1.9
-   Renders Django projects with 100% starting test coverage
-   Twitter Bootstrap v4.0.0 - alpha
-   Continuous integration with Concourse CI
-   ReactJS
-   12-Factor based settings via django-environ
-   Optimized development and production settings
-   Registration via django-auth-ldap to internal Active Directory environments
-   Comes with custom user model ready to go.
-   Grunt build for compass and livereload
-   Docker support using docker-compose for development and production
-   Python 3.5.x
-   Run tests with unittest or py.test!

Optional Integrations
---------------------

*These features can be enabled during initial project setup.*
-   Integration with MailHog (https://github.com/mailhog/MailHog) for
local email testing
-   Configuration for Celery (http://www.celeryproject.org)
-   Configuration for Redis (http://redis.io)

Constraints
-----------

-   Only maintained 3rd party libraries are used.
-   PostgreSQL everywhere (9.0+)
-   Environment variables for configuration (This won't work
    with Apache/mod\_wsgi).

Usage
-----

Let's pretend you have an internal network with the following services:
- Yum package manager
- PyPI package manager
- Concourse CI
- Docker Repository


You want to create a Django project called "redditclone".
Rather than using startproject and then editing the results to include
your name, email, and various configuration issues that always get
forgotten until the worst possible moment, use cookiecutter to do all the
work.

First, get cookiecutter. Trust me, it's awesome:

    $ pip install cookiecutter

Now run it against this repo:

    $ cookiecutter https://your-bitbucket.com/scm/cookiecutter-django-dc.git

You'll be prompted for some questions, answer them, then it will create
a Django project for you.

**Warning**: After this point, change 'Daniel Greenfeld', 'pydanny', etc
to your own information.

**Warning**: repo\_name must be a valid Python module name or you will
have issues on imports.

It prompts you for questions. Answer them:

    Cloning into 'cookiecutter-django-dc'...
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
    now [2016/03/30]: 2016/03/30
    year [2016]:
    use_celery [n]: n
    use_mailhog [n]: n
    use_redis [n]: n
    windows [n]: n
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
    $ git remote add origin https://your-bitbucket.com:scm/redditclone.git
    $ git push -u origin master

Now take a look at your repo. Don't forget to carefully look at the
generated README. Awesome, right?

For development, see the following for local development:

-   Developing
    locally (http://cookiecutter-django.readthedocs.org/en/latest/developing-locally.html)
-   Developing locally using
    docker (http://cookiecutter-django.readthedocs.org/en/latest/developing-locally-docker.html)

Articles
--------

-   Development and Deployment of Cookiecutter-Django via
    Docker (https://realpython.com/blog/python/development-and-deployment-of-cookiecutter-django-via-docker)
-   Development and Deployment of Cookiecutter-Django on
    Fedora (https://realpython.com/blog/python/development-and-deployment-of-cookiecutter-django-on-fedora/)


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
