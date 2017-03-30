Testare specifici file
======================

Volendo possiamo eseguire i test su
alcuni file, piuttosto che su tutto
il progetto:

.. code-block:: shell

   $ sphinx-build -b doctest . build/doctest \
   options.rst first_example.rst

Ci troviamo sul branch ``08_test_specific_files``.
