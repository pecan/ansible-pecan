ansible-pecan
=============
A playbook to deploy Pecan applications. It is initially a bit opinionated
choosing nginx for the web server and `circus <https://circus.readthedocs.org/en/latest/>`_
for managing the services.

Currently supported distributions:

* Ubuntu Trusty (14.04)

ssl
---
When ``use_ssl`` is set to ``true`` (the default) the playbook will create
self-signed ssl certificates for you *unless* ``self_signed`` is set to
``false`` (defaults to ``true``).

vars
----
There is only one variable that must be defined: ``app_name``. This will be
used to create directories, name log files, and configure other pieces like
Circus.

The rest of the variables are optional, and are listed here with their default
values:

* app_home: /opt/{{ app_name }}
* wsgi_file: wsgi.py
* wsgi_callable: application
* branch: "master"
* use_nginx: true
* use_ssl: true
* self_signed: true
