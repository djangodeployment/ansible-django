======
Django
======

Overview
========

This is an Ansible role for deploying a Django application on a Debian
(>=8) or Ubuntu LTS (>=16) server. It uses nginx, Gunicorn, systemd and
sqlite3.

Variables
=========

- ``django_project``: The name of the project (used for directory
  names).
- ``django_project_repository``: The git repository from which to
  download the django project.
- ``django_user``: The name of the user (and group) as which Django will
  run.
- ``django_project_python``: Either "python" or "python3".
- ``django_project_site_packages``: Use "yes" to use
  ``--system-site-packages`` in the virtualenv.
- ``django_domain``: The domain name in which the app will be installed.
- ``django_secret_key``: The Django ``SECRET_KEY``.
- ``django_port``: The port in which Gunicorn will be listening.
- ``gunicorn_workers``: The number of gunicorn workers.

Meta
====

Written by Antonis Christofides

| Copyright (C) 2017 Antonis Christofides

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see http://www.gnu.org/licenses/.
