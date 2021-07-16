|test|_

About
=====

Logging facilities in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-log

An example
==========

.. code-block:: python

   from log import get_logger

   def main():
       logger = get_logger(__name__)
       logger.warning(f"Is 1 + 1 = {1 + 2} really correct?")
       logger.error(f"Something is wrong!")

The output:

.. code-block:: text

   $ mys run
   basic.main WARNING Is 1 + 1 = 3 really correct?
   basic.main ERROR Something is wrong!

API
===

.. mysfile:: src/lib.mys

.. |test| image:: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml

.. _Mys programming language: https://mys-lang.org
