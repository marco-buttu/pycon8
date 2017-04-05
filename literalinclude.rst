``download`` e ``literalinclude``
=================================

Supponiamo di avere il seguente modulo:

.. code-block:: python

   class Foo:
       def foo(self):
           print('pycon8')

Ecco un esempio di codice che utilizza questo modulo:

.. doctest::

   >>> from mymodule import Foo
   >>> obj = Foo()
   >>> obj.foo()
   pycon8

Ci troviamo sul branch ``09_literalinclude``.
