<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# Django Example for YunoHost

[![Integration level](https://dash.yunohost.org/integration/django_example_ynh.svg)](https://dash.yunohost.org/appci/app/django_example_ynh) ![Working status](https://ci-apps.yunohost.org/ci/badges/django_example_ynh.status.svg) ![Maintenance status](https://ci-apps.yunohost.org/ci/badges/django_example_ynh.maintain.svg)  
[![Install Django Example with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=django_example_ynh)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install Django Example quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

[![tests](https://github.com/YunoHost-Apps/django_example_ynh/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/YunoHost-Apps/django_example_ynh/actions/workflows/tests.yml)
[![codecov](https://codecov.io/github/jedie/django_example_ynh/branch/main/graph/badge.svg)](https://codecov.io/github/jedie/django_example_ynh)
[![django_example_ynh @ PyPi](https://img.shields.io/pypi/v/django_example_ynh?label=django_example_ynh%20%40%20PyPi)](https://pypi.org/project/django_example_ynh/)
[![Python Versions](https://img.shields.io/pypi/pyversions/django_example_ynh)](https://github.com/YunoHost-Apps/django_example_ynh/blob/main/pyproject.toml)
[![License GPL-3.0](https://img.shields.io/pypi/l/django_example_ynh)](https://github.com/YunoHost-Apps/django_example_ynh/blob/main/LICENSE)

Demo [YunoHost Application](https://install-app.yunohost.org/?app=django_example_ynh) to demonstrate the integration of a [Python](https://www.python.org/)/[Django](https://www.djangoproject.com/) project under YunoHost using [django_yunohost_integration](https://github.com/YunoHost-Apps/django_yunohost_integration).

To demonstrate the functionality the small [django-example](https://github.com/jedie/django-example) app will be installed.

[![Integration level](https://dash.yunohost.org/integration/django_example_ynh.svg)](https://dash.yunohost.org/appci/app/django_example_ynh) ![](https://ci-apps.yunohost.org/ci/badges/django_example_ynh.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/django_example_ynh.maintain.svg)
[![Install django_example_ynh with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=django_example_ynh)


Pull requests welcome ;)


**Shipped version:** 0.2.0~ynh1
## Disclaimers / important information

## local test

For quicker developing of django_example_ynh in the context of YunoHost app,
it's possible to run the Django developer server with the settings
and urls made for YunoHost installation.

e.g.:
```bash
~$ git clone https://github.com/YunoHost-Apps/django_example_ynh.git
~$ cd django_example_ynh/
~/django_example_ynh$ make
install-poetry         install or update poetry
install                install project via poetry
update                 update the sources and installation and generate "conf/requirements.txt"
lint                   Run code formatters and linter
fix-code-style         Fix code formatting
tox-listenvs           List all tox test environments
tox                    Run pytest via tox with all environments
pytest                 Run pytest
publish                Release new version to PyPi
local-test             Run local_test.py to run the project locally
local-diff-settings    Run "manage.py diffsettings" with local test

~/django_example_ynh$ make install-poetry
~/django_example_ynh$ make install
~/django_example_ynh$ make local-test
```

Notes:

* SQlite database will be used
* A super user with username `test` and password `test` is created
* The page is available under `http://127.0.0.1:8000/app_path/`


## history

* [compare v0.1.5...master](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.2.0...master) **dev**
  * tbc
* [v0.2.0 - 15.09.2021](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.1.5...v0.2.0)
  * rename/split `django_example_ynh` into:
    * [django_yunohost_integration](https://github.com/jedie/django_yunohost_integration) - Python package with the glue code to integrate a Django project with YunoHost
    * [django_example_ynh](https://github.com/YunoHost-Apps/django_example_ynh) - Demo YunoHost App to demonstrate the integration of a Django project under YunoHost
* [v0.1.5 - 19.01.2021](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.1.4...v0.1.5)
  * Make some deps `gunicorn`, `psycopg2-binary`, `django-redis`, `django-axes` optional
* [v0.1.4 - 08.01.2021](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.1.3...v0.1.4)
  * Bugfix [CSRF verification failed on POST requests #7](https://github.com/YunoHost-Apps/django_example_ynh/issues/7)
* [v0.1.3 - 08.01.2021](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.1.2...v0.1.3)
  * set "DEBUG = True" in local_test (so static files are served and auth works)
  * Bugfixes and cleanups
* [v0.1.2 - 29.12.2020](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.1.1...v0.1.2)
  * Bugfixes
* [v0.1.1 - 29.12.2020](https://github.com/YunoHost-Apps/django_example_ynh/compare/v0.1.0...v0.1.1)
  * Refactor "create_superuser" to a manage command, useable via "django_example_ynh" in `INSTALLED_APPS`
  * Generate "conf/requirements.txt" and use this file for install
  * rename own settings and urls (in `/conf/`)
* [v0.1.0 - 28.12.2020](https://github.com/YunoHost-Apps/django_example_ynh/compare/f578f14...v0.1.0)
  * first working state
* [23.12.2020](https://github.com/YunoHost-Apps/django_example_ynh/commit/f578f144a3a6d11d7044597c37d550d29c247773)
  * init the project


## Links

* Report a bug about this package: https://github.com/YunoHost-Apps/django_example_ynh
* YunoHost website: https://yunohost.org/
* PyPi package: https://pypi.org/project/django-ynh/

These projects used `django_example_ynh`:

* https://github.com/YunoHost-Apps/django_example_ynh
* https://github.com/YunoHost-Apps/django-for-runners_ynh

---

# Developer info

The App project will be stored under `__FINALPATH__` (e.g.: `/opt/yunohost/$app`) that's Django's `settings.FINALPATH`
"static" / "media" files to serve via nginx are under `__PUBLIC_PATH__` (e.g.: `/var/www/$app`) that's `settings.PUBLIC_PATH`

## package installation / debugging

This app is not in YunoHost app catalog. Test install, e.g.:
```bash
~# git clone https://github.com/YunoHost-Apps/django_example_ynh.git
~# yunohost app install django_example_ynh/ -f
```
To update:
```bash
~# cd django_example_ynh
~/django_example_ynh# git fetch && git reset --hard origin/testing
~/django_example_ynh# yunohost app upgrade django_example_ynh -u . -F
```

To remove call e.g.:
```bash
sudo yunohost app remove django_example_ynh
```

Backup / remove / restore cycle, e.g.:
```bash
yunohost backup create --apps django_example_ynh
yunohost backup list
archives:
  - django_example_ynh-pre-upgrade1
  - 20201223-163434
yunohost app remove django_example_ynh
yunohost backup restore 20201223-163434 --apps django_example_ynh
```

Debug the installation, e.g.:
```bash
root@yunohost:~# cat /etc/yunohost/apps/django_example_ynh/settings.yml
...

root@yunohost:~# ls -la /var/www/django_example_ynh/
total 18
drwxr-xr-x 4 root root 4 Dec  8 08:36 .
drwxr-xr-x 6 root root 6 Dec  8 08:36 ..
drwxr-xr-x 2 root root 2 Dec  8 08:36 media
drwxr-xr-x 7 root root 8 Dec  8 08:40 static

root@yunohost:~# ls -la /opt/yunohost/django_example_ynh/
total 58
drwxr-xr-x 5 django_example_ynh django_example_ynh   11 Dec  8 08:39 .
drwxr-xr-x 3 root        root           3 Dec  8 08:36 ..
-rw-r--r-- 1 django_example_ynh django_example_ynh  460 Dec  8 08:39 gunicorn.conf.py
-rw-r--r-- 1 django_example_ynh django_example_ynh    0 Dec  8 08:39 local_settings.py
-rwxr-xr-x 1 django_example_ynh django_example_ynh  274 Dec  8 08:39 manage.py
-rw-r--r-- 1 django_example_ynh django_example_ynh  171 Dec  8 08:39 secret.txt
drwxr-xr-x 6 django_example_ynh django_example_ynh    6 Dec  8 08:37 venv
-rw-r--r-- 1 django_example_ynh django_example_ynh  115 Dec  8 08:39 wsgi.py
-rw-r--r-- 1 django_example_ynh django_example_ynh 4737 Dec  8 08:39 django_example_ynh_demo_settings.py

root@yunohost:~# cd /opt/yunohost/django_example_ynh/
root@yunohost:/opt/yunohost/django_example_ynh# source venv/bin/activate
(venv) root@yunohost:/opt/yunohost/django_example_ynh# ./manage.py check
django_example_ynh v0.8.2 (Django v2.2.17)
DJANGO_SETTINGS_MODULE='django_example_ynh_demo_settings'
PROJECT_PATH:/opt/yunohost/django_example_ynh/venv/lib/python3.7/site-packages
BASE_PATH:/opt/yunohost/django_example_ynh
System check identified no issues (0 silenced).

root@yunohost:~# tail -f /var/log/django_example_ynh/django_example_ynh.log
root@yunohost:~# cat /etc/systemd/system/systemd.service
...

root@yunohost:~# systemctl reload-or-restart django_example_ynh
root@yunohost:~# journalctl --unit=django_example_ynh --follow
```



## Documentation and resources

* Official app website: <https://github.com/YunoHost-Apps/django_example_ynh>
* Official user documentation: <https://github.com/jedie/django-example>
* Official admin documentation: <https://github.com/YunoHost-Apps/django_example_ynh>
* Upstream app code repository: <https://github.com/YunoHost-Apps/django_example_ynh>
* YunoHost documentation for this app: <https://yunohost.org/app_django_example_ynh>
* Report a bug: <https://github.com/YunoHost-Apps/django_example_ynh_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/django_example_ynh_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/django_example_ynh_ynh/tree/testing --debug
or
sudo yunohost app upgrade django_example_ynh -u https://github.com/YunoHost-Apps/django_example_ynh_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
