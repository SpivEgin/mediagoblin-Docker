Dockerized http://mediagoblin.org/
==================================

Demo MediaGoblin
----------------

All data are lost when the container is stopped.

    sudo docker run -p 8080:80 spivegin/mediagoblin
    www-browser http://localhost:8080

The default user is admin, password CoNi4NGERsUbUMmUGHt

Demo MediaGoblin locally
------------------------

The image is built locally, there is no dependency to the Docker registry. All data are lost when the container is stopped.

    git clone https://github.com/SpivEgin/mediagoblin-Docker.git
    sudo docker build -t mediagoblin-demo mediagoblin-docker
    sudo docker run -p 8080:80 mediagoblin-docker
    www-browser http://localhost:8080

The default user is admin, password CoNi4NGERsUbUMmUGHt

Run MediaGoblin
---------------

The data is preserved in /srv/mediagoblin.

    git clone https://github.com/SpivEgin/mediagoblin-Docker.git
    sudo docker build -t mediagoblin-demo mediagoblin-docker
    sudo mkdir /srv/mediagoblin
    sudo docker --name mediagoblin run -p 8080:80 \
         -v /srv/mediagoblin:/var/lib/mediagoblin \
         mediagoblin-docker
    www-browser http://localhost:8080

The default user is admin, password CoNi4NGERsUbUMmUGHt
