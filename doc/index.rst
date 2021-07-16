|test|_

About
=====

Logging facilities in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-log

Example
=======

.. code-block:: python

   from log import Logger

   def main():
       logger = Logger("log-main")
       logger.info(f"1 + 1 = {1 + 1}")

Functions and types
===================

.. mysfile:: src/lib.mys

.. |test| image:: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml

.. _Mys programming language: https://mys-lang.org
