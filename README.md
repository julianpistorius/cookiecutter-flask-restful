Cookiecutter Flask RESTful
==========

This is a basic boilerplate app that can be used with Cookiecutter
to scaffold new flask restful application.

> If you find a bug in project, please open a ticket.


## Installation and Usage
```sh
$ mkdir ~/flaskProjects
$ cd flaskProjects
$ virtualenv venv
$ source venv/bin/activate
(venv) $ cookiecutter gh:xk0nsid/cookiecutter-flask-restful
```

Answer the asked questions properly.

```sh
(venv) $ cd project_name
(venv) $ pip install -r requirements.txt
(venv) $ python manage.py db init
(venv) $ python manage.py db migrate
(venv) $ python manage.py db upgrade
(venv) $ python manage.py runserver
```

## Features

The app comes with some  basic stuff. Like Basic user model. Basic views for
the user etc. Below is the list of avalable endpoints

### Endpoints

|             URI               |     Protected     |    HTTP Method    |             Action
|:---------                     |:--:               |:--:               |--:
| **/version/version/users/**   | Yes               | GET               | Get list of all users
| **/version/users/**           | No                | POST              | Create a new user
| **/version/users/**           | No                | OPTIONS           | Help for the given endpoint
| **/version/users/user_id**    | Yes               | GET               | Get data of a single user
| **/version/users/user_id**    | No                | OPTIONS           | Help for the given endpoint
| **/auth/**                    | No                | GET               | Request auth token
