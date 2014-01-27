django-gae-skeleton
===================

A Django (1.5) project skeleton. Running Django on Google appengine with 
Cloud SQL as database backend

Meta
====

* author: Janny Kinende
* email:  janny.kinende@gmail.com
* status: maintained, in development
* notes:  Have feedback? Please send me an email. This project is still in its
          development, and will be changing rapidly.


Purpose
=======

This project is meant to be a boilerplate project for starting development. It
is heavily opinionated in terms of services and tools--but I think the tradeoff
is worthwhile.

Essentially--deploying Django projects is hard. There are lots of things you
need to take into consideration. Being a Django user for  almost 2 years now, I believe I've
found some extremely useful patterns to help manage all sorts of Django sites
(from the very smallest apps, to the largest).


Docs
====

The full project documentation is hosted at RTFD: http://jarixsoft.com
They are continuously updated to reflect changes and information about the
project, so be sure to read them before using this boilerplate.


Install
=======

django-gae-skeleton currently supports Django 1.5. To create a new django-gae-skeleton base
project, run the following command (this assumes you have the google appengine sdk (python) 
installed already):

    $ django-admin.py startproject --template=https://github.com/JannyK/django-gae-skeleton/zipball/master projectname


Where "projectname" is the name of the project you'd like to create.

This is possible because Django 1.5's ``startproject`` command allows you to
fetch a project template over HTTP (which is what we're doing here).


The production settings pull SECRET_KEY from environment but fallbacks
to a value which is generated mainly for development environment.

This setup allows you to easily keep your site in a public repo if you so 
wish without causing opening a route to attack your Django passwords.