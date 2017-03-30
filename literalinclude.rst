``download`` e ``literalinclude``
=================================

Supponiamo di avere il seguente modulo
:download:`mymodule.py <include/mymodule.py>`:

.. literalinclude:: include/mymodule.py
   :language: python

Ecco un esempio di codice che utilizza questo modulo:

.. doctest::

   >>> from mymodule import Foo
   >>> obj = Foo()
   >>> obj.foo()
   pycon8

Ci troviamo sul branch ``09_literalinclude``.
