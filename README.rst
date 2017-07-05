Nginx
=====

Configuration
-------------

Using nginx-light

The supplied ``nginx.conf`` sets up the appropriate configuration for running
locally out of the repository directory. 

Essentially, requests for static files are handled by `Nginx`_, requests for API endpoints are proxied to port 8081.

Running
-------

.. code:: sh

    nginx -c nginx.conf -p $(pwd)


.. _Nginx: https://www.nginx.com/

Stopping
--------

``nginx -s stop``
  
Troubleshooting
---------------

https://blog.serverdensity.com/troubleshoot-nginx/


TODO
----

npm target script
^^^^^^^^^^^^^^^^^
In dev source package.json


``clean-build: rm -rf  nginx-ng4/static; rm -rf  nginx-ng4/index.html;``

``cp -r <dev-source>/dist/* nginx-ng4/``

Size
----
.. code:: sh

    256 K	./static/css
    1.2 M	./static/js
    576 B    index.html

    $ tree --du
    .
    ├── [        748]  README.rst
    ├── [        576]  index.html
    ├── [        781]  nginx.conf
    └── [    1349007]  static
        ├── [     111865]  css
        │   └── [     111763]  app.4501fb4f10377d7f30bb.css
        └── [    1237006]  js
            ├── [     147170]  app.4501fb4f10377d7f30bb.js
            ├── [     111712]  polyfills.4501fb4f10377d7f30bb.js
            └── [     977954]  vendor.4501fb4f10377d7f30bb.js

     1351384 bytes used in 3 directories, 7 files

Prerquisite
-----------

nginx  `nginx-light`

https://askubuntu.com/questions/553937/what-is-the-difference-between-the-core-full-extras-and-light-packages-for-ngi

https://packages.debian.org/sid/nginx-light
