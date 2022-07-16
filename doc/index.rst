|discord|_
|test|_
|stars|_

About
=====

Logging facilities in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-log

A basic example
===============

Create a logger and call it's warning and error methods to print
messages to standard output.

.. code-block:: mys

   from log import get_logger

   func main():
       logger = get_logger(__name__)
       logger.WARNING(f"Is 1 + 1 = {1 + 2} really correct?")
       logger.ERROR(f"Something is wrong!")

The output:

.. code-block:: myscon

   ❯ mys run
    ✔ Reading package configuration (0 seconds)
    ✔ Building (1.43 seconds)
   basic.main WARNING Is 1 + 1 = 3 really correct?
   basic.main ERROR Something is wrong!

Setting logging level example
=============================

Set a logger's level by just knowing the logger name.

.. code-block:: mys

   from log import get_logger
   from log import LOGGERS
   from log import Level

   func set_log_level_to_debug(name: string):
       logger = LOGGERS.get(name, None)

       if logger is None:
           print(f"Logger '{name}' does not exist.")
       else:
           logger.level = Level.Debug

   func main():
       logger = get_logger("foo")

       logger.DEBUG("First try.")

       set_log_level_to_debug("bar")
       logger.DEBUG("Second try.")

       set_log_level_to_debug("foo")
       logger.DEBUG("Third try.")

The output:

.. code-block:: myscon

   ❯ mys run
    ✔ Reading package configuration (0 seconds)
    ✔ Building (2.13 seconds)
   Logger 'bar' does not exist.
   Setting log level to debug for logger 'foo'.
   foo DEBUG Third try.

API
===

.. mysfile:: src/lib.mys

.. |discord| image:: https://img.shields.io/discord/777073391320170507?label=Discord&logo=discord&logoColor=white
.. _discord: https://discord.gg/GFDN7JvWKS

.. |test| image:: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml

.. |stars| image:: https://img.shields.io/github/stars/mys-lang/package-log?style=social
.. _stars: https://github.com/mys-lang/package-log

.. _Mys programming language: https://mys-lang.org
