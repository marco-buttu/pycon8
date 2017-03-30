Indicare la versione di Python
==============================

A partire da `Sphinx 1.6
<https://github.com/sphinx-doc/sphinx>`_
sarà possibile saltare dei test nel caso
in cui la versione di Python sia diversa
da quella specificata.  Ad esempio, nel
seguente caso i test verranno eseguiti
solamente se si sta utilizzando
Python >= 3.6:

.. doctest::
   :pyversion: >= 3.6

   >>> name, surname = 'Enrico', 'Fermi'
   >>> f'Mi chiamo {name} {surname}'
   'Mi chiamo Enrico Fermi'

Come possiamo vedere, se usiamo Python 3.7
allora i 2 test del precedente esempio
vengono eseguiti:

.. code-block:: shell

   $ python --version
   Python 3.7.0a0
   $ sphinx-build -b doctest . build/doctest pyversion.rst
       ...
   Doctest summary
   ===============
       2 tests
       ...
   build succeeded

Se invece usiamo Python 3.5.1, allora
il report indicherà che non è stato
eseguito alcun test:

.. code-block:: shell

   $ python --version
   Python 3.5.1
   $ sphinx-build -b doctest . build/doctest pyversion.rst
       ...
   Doctest summary
   ===============
       0 tests
       ...
   build succeeded

Ci troviamo sul branch ``10_pyversion``.
