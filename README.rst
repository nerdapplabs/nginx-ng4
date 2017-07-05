Nginx
=====

Configuration
-------------

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

256K	./static/css
1.2M	./static/js

