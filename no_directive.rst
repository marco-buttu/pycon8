Direttiva ``doctest`` non necessaria
====================================

La direttiva ``doctest`` non è necessaria.
Il seguente esempio infatti viene testato:

   >>> print('pycon8')
   pycon8

Possiamo utilizzare le `option flags
<https://docs.python.org/3/library/doctest.html#option-flags>`
del modulo ``doctest`` senza dover necessariamente
far ricorso alla direttiva ``doctest``.  Ad esempio,
consideriamo questo test:

.. doctest::
   :options: +NORMALIZE_WHITESPACE

   >>> from decimal import Decimal
   >>> numbers = '1.34 1.87 3.45 2.35 1.00 0.03 9.25'
   >>> data = list(map(Decimal, numbers.split()))
   >>> sorted(data)
   [Decimal('0.03'), Decimal('1.00'), Decimal('1.34'),
    Decimal('1.87'), Decimal('2.35'), Decimal('3.45'),
    Decimal('9.25')]

Possiamo scriverlo anche così:

   >>> numbers = '1.34 1.87 3.45 2.35 1.00 0.03 9.25'
   >>> data = list(map(Decimal, numbers.split()))
   >>> sorted(data)  # doctest: +NORMALIZE_WHITESPACE
   [Decimal('0.03'), Decimal('1.00'), Decimal('1.34'),
    Decimal('1.87'), Decimal('2.35'), Decimal('3.45'),
    Decimal('9.25')]

La direttiva ``doctest`` è invece necessaria
quando vogliamo eseguire ``testsetup`` o
``testclenup``, oppure l'opzione ``pyversion``,
dato che queste non sono *option flags* del modulo
`doctest <https://docs.python.org/3/library/doctest.html>`_
della libreria standard ma dell'estensione
`ext.sphinx.doctest
<http://www.sphinx-doc.org/en/stable/ext/doctest.html>`_
di Sphinx.

Infine, se usiamo due volte i due punti (``::``), allora
il test sull'esempio verrà saltato, come nel seguente
caso::

   >>> a = 33
   >>> print(a)  # Il test non fallisce
   44

Ci troviamo sul branch ``11_no_directive``.
