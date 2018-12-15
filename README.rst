
.. image:: https://img.shields.io/docker/stars/practicalci/alpine-glibc.svg?style=flat-square
   :target: https://hub.docker.com/r/practicalci/alpine-glibc/
   :alt: Docker Stars

.. image:: https://img.shields.io/docker/pulls/practicalci/alpine-glibc.svg?style=flat-square
   :target: https://hub.docker.com/r/practicalci/alpine-glibc/
   :alt: Docker Pulls


Alpine GNU C library (glibc) Docker image
=========================================

This image is based on Alpine Linux image, which is only a 5MB image, and contains glibc to enable
proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

This image includes some quirks to make `glibc <https://www.gnu.org/software/libc/>`_ work side by
side with musl libc (default in Alpine Linux). glibc packages for Alpine Linux are prepared by
`Sasha Gerrand`_ and the releases are published in
`sgerrand/alpine-pkg-glibc`_ github repo.

.. _`Sasha Gerrand`: https://github.com/sgerrand
.. _`sgerrand/alpine-pkg-glibc`: https://github.com/sgerrand/alpine-pkg-glibc

Download size of this image is only:

.. image:: https://images.microbadger.com/badges/image/practicalci/alpine-glibc.svg
   :target: http://microbadger.com/images/practicalci/alpine-glibc


Usage Example
-------------

This image is intended to be a base image for your projects, so you may use it like this:
::

    Dockerfile
        FROM frolvlad/alpine-glibc
        
        COPY ./my_app /usr/local/bin/my_app

::

    sh
    $ docker build -t my_app .


Attributions
============

This work is derived from `frol/docker-alpine-glibc`_ , `Vlad Frolov`_ work.

.. _`Vlad Frolov`: https://github.com/frol
.. _`frol/docker-alpine-glibc`: https://github.com/frol/docker-alpine-glibc


Original licenses and attributions are are kept in `attributions`_ folder.

.. _`attributions`: ./attributions/ATTRIBUTIONS.rst

