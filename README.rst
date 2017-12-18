datefinder - extract dates from text using RE2
====================================

A python module for locating dates inside text. Use this package to extract all sorts 
of date like strings from a document and turn them into datetime objects.

This module finds the likely datetime strings and then uses the  
`dateparser <https://github.com/scrapinghub/dateparser>`_ package to convert 
to the datetime object.


Installation
------------
 Install re2 from https://github.com/google/re2
 Install pyre2 from https://github.com/axiak/pyre2 (you can use a variant fork of pyre2 but the build and capability nuances are upto your study. Will be delighted to hear if there is a value addition using some other fork than axiak.)
   
.. code-block:: sh
    $git clone git://github.com/SandeepNaidu/datefinder.git
    $ cd datefinder.git
    $ python setup.py install
    

How to Use
----------


.. automodule:: datefinder
   :members: find_dates


.. code-block:: python

    In [1]: string_with_dates = """
       ...: ...
       ...: entries are due by January 4th, 2017 at 8:00pm
       ...: ...
       ...: created 01/15/2005 by ACME Inc. and associates.
       ...: ...
       ...: """

    In [2]: import datefinder

    In [3]: matches = datefinder.find_dates(string_with_dates)

    In [4]: for match in matches:
       ...:     print match
       ...:
    2017-01-04 20:00:00
    2005-01-15 00:00:00

Thanks
------
Thanks to Google, Facebook, @axaik and @akoumjian for their code on which these changes stand.

Support
-------

`github <https://github.com/SandeepNaidu/datefinder/issues/>`_. 

Disclaimer
----------
Authors do not have any liability directly or indirectly to any kind of loss incurred from the use of the software directly or indirectly. Use it at your own risk.

