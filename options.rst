Opzioni
=======

Questo è un esempio in cui si utilizzano i tre
punti per indicare che si sta omettendo del testo:

.. doctest::

   >>> import statistics
   >>> dir(statistics)
   ['Decimal', 'Fraction', 'StatisticsError', ..., 'variance']

Qua invece si utilizza l'opzione ``NORMALIZE_WHITESPACE``
per rimuovere i newline e gli spazi vuoti dall'output.
Questo ci consente di suddividere l'output su più linee:

.. doctest::
   :options: +NORMALIZE_WHITESPACE

   >>> import statistics
   >>> dir(statistics)
   ['Decimal',
    'Fraction',
    'StatisticsError',
       ...
    'variance']

L'ellipsis è molto utile per nascondere parte
del traceback, in modo da rendere l'esempio
più leggibile:

.. doctest::

   >>> print(z)
   Traceback (most recent call last):
       ...
   NameError: name 'z' is not defined

Se nell'output c'è una linea vuota, nel file
:file:`rst` dobbiamo sostituirla con ``<BLANKLINE>``.
Ovviamente il testo ``<BLANKLINE>`` non comparirà
nell'output, come possiamo vedere dal seguente esempio:

.. doctest::

   >>> print('\nPython 3')
   <BLANKLINE>
   Python 3


Se per qualche motivo vogliamo saltare un test,
ad esempio perché il risultato non è deterministico,
usiamo l'opzione ``SKIP``:

.. doctest::

   >>> import random
   >>> random.randrange(1000)  # doctest: +SKIP
   996

Per eseguire i test e creare la documentazione in
HTML, ponendoci nel punto in cui ci troviamo adesso:

.. code-block:: shell

   $ git checkout 04_options
   $ make doctest
   $ make html
