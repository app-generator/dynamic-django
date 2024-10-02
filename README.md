# [Dynamic Django](https://github.com/app-generator/dynamic-django)

**Dynamic Programming Patterns** applied in `Python/Django` - Actively supported by [AppSeed](https://appseed.us/). 

For support create a new issue on the REPO or send an email to `support@appseed.us`.  

## Features 

- [OK] Dynamic API via DRF
- [WIP] Dynamic DT
- [WIP] Models Editor
- [WIP] Configuration Updater       

## Quick Start

```
# Clone Repo
$ git clone https://github.com/app-generator/dynamic-django.git
```

> Create VENV

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install -r requirements.txt
```

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

> Start the Project

```bash
$ python manage.py createsuperuser # create the admin
$ python manage.py runserver       # start the project
```

## Update model 

```bash
$ python
>>> from cli import *
>>> add_model('home', 'Stats')
>>> # Syntax: model_add_field('APP_NAME_HERE', 'MODEL_NAME_HERE', 'FIELD_NAME',  'FIELD_TYPE') 
>>> add_model_field('home', 'Stats', 'aInt',  'int') 
>>> add_model_field('home', 'Stats', 'aChar', 'str')
>>> add_model_field('home', 'Stats', 'aText', 'text')
```

The file is automatically reformated using `black` and DB migrated.

## DB Backup / RESET / Restore

```bash
$ python manage.py dbbackup  -o 20240930-001.dump  # backup 
$ python manage.py reset_db                        # RESET_DB [ Danger, all tables wipped ]
$ python manage.py dbrestore -i 20240930-001.dump  # restore 
```

---
[Dynamic Django](https://github.com/app-generator/dynamic-django) - Open-source project crafted by AppSeed 
