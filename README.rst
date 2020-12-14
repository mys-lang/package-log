|buildstatus|_

Log
===

Logging facilities in the `Mys programming language`_.

Examples
========

.. code-block:: python

   from log import Logger

   def main():
       logger = Logger("log-main")
       logger.info("1 + 1 = {}", 1 + 1)

.. |buildstatus| image:: https://travis-ci.com/eerimoq/mys-log.svg?branch=master
.. _buildstatus: https://travis-ci.com/eerimoq/mys-log

.. _Mys programming language: https://github.com/eerimoq/mys
