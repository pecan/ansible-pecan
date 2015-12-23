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

* ``app_home: /opt/{{ app_name }}``
* ``wsgi_file: wsgi.py``
* ``wsgi_callable: application``
* ``branch: "master"``
* ``use_nginx: true``
* ``use_ssl: true``
* ``self_signed: true``

LICENSE
=======
The MIT License (MIT)

Copyright (c) 2015 ansible-pecan contributors
---------------------------------------------
*ansible-pecan contributors listed on* `AUTHORS file <https://github.com/pecan/ansible-pecan/blob/master/AUTHORS>`_

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
