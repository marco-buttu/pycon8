Raggruppare i test
==================

É possibile raggruppare i test specificando
il nome del gruppo nelle direttive ``testsetup``,
``doctest`` e ``testcleanup``.  Ad esempio,
questo file contiene una certa serie di esempi.
Questo è il primo:

.. doctest::

   >>> a = 33
   >>> print(a)
   33

Questo è il secondo:

.. doctest::

   >>> b = a + 67
   >>> print(b)
   100

Infine c'è questo esempio:

.. testsetup:: math_sqrt

   import math
   sqrt = math.sqrt

.. doctest:: math_sqrt

   >>> import math
   >>> math.sqrt(25)
   5.0
   >>> math.sqrt
   <built-in function sqrt>
   >>> math.sqrt = 33
   >>> math.sqrt
   33

.. testcleanup:: math_sqrt

   math.sqrt = sqrt

Vogliamo che il ``testsetup`` e il ``testcleanup``
vengano eseguiti solamente prima dell'ultimo
``doctest``, e non negli altri, per cui li
raggruppiamo sotto lo stesso nome (``math_sqrt``).

Ci troviamo sul branch ``06_groups``.
