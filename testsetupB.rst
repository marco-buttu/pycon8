We are all adults here
======================

Ad esempio, possiamo fare questo:

.. testsetup::

   import math
   sqrt = math.sqrt

.. doctest::

   >>> import math
   >>> math.sqrt(25)
   5.0
   >>> math.sqrt
   <built-in function sqrt>
   >>> math.sqrt = 33
   >>> math.sqrt
   33

.. testcleanup::

   math.sqrt = sqrt

Ci troviamo sul branch ``05_setup_cleanup``.
