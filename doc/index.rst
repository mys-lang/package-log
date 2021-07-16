|test|_

About
=====

Logging facilities in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-log

A basic example
---------------

Create a logger and call it's warning and error methods to print
messages to standard output.

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

Setting logging level example
-----------------------------

Set a logger's level by just knowing the logger name.

.. code-block:: python

   from log import get_logger
   from log import LOGGERS
   from log import Level

   def set_log_level_to_debug(name: string):
       logger = LOGGERS.get(name, None)

       if logger is None:
           print(f"Logger '{name}' does not exist.")
       else:
           logger.level = Level.Debug

   def main():
       logger = get_logger("foo")

       logger.debug("First try.")

       set_log_level_to_debug("bar")
       logger.debug("Second try.")

       set_log_level_to_debug("foo")
       logger.debug("Third try.")

The output:

.. code-block:: text

   $ mys run
   Logger 'bar' does not exist.
   Setting log level to debug for logger 'foo'.
   foo DEBUG Third try.

API
===

.. mysfile:: src/lib.mys

.. |test| image:: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-log/actions/workflows/pythonpackage.yml

.. _Mys programming language: https://mys-lang.org
