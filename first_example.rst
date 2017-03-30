Primo esempio
=============

Questo è un primo esempio di codice:

.. doctest::

   >>> import math
   >>> result = math.log(1)
   >>> result
   0.0

Per verificare che l'esempio funzioni
correttamente, diamo il comando
``make doctest``:

.. code-block:: shell

   $ make doctest
       ...
   Doctest summary
   ===============
       3 tests
       0 failures in tests
       0 failures in setup code
       0 failures in cleanup code
   build succeeded.

Il namespace si conserva da un esempio
al successivo.  Nel seguente esempio
infatti non importiamo ``math``, visto
che è già stato importato in precedenza,
e possiamo usare ``result``:

.. doctest::

   >>> math.cos(0)
   1.0
   >>> result
   0.0

Per eseguire i test e creare la documentazione
in HTML (nel punto in cui ci troviamo adesso):

.. code-block:: shell

   $ git checkout 03_first_example
   $ make doctest
   $ make html
