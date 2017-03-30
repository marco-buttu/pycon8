Global setup
============

Questo esempio non avrebbe funzionato
se non avessimo modificato il file
:file:`conf.py` definendo oppurtunamente
``doctest_global_setup``:

.. doctest::

   >>> a = 33
   >>> import __main__
   >>> __main__.a
   33

Ci troviamo sul branch ``07_global_setup``.
