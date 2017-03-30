Installazione di Sphinx
=======================

Prima di tutto installiamo `Sphinx
<http://www.sphinx-doc.org/en/stable/>`_:

.. code-block:: shell

   $ pip install sphinx

A questo punto creiamo un progetto, usando il
comando ``sphinx-quickstart``:

.. code-block:: shell

   $ sphinx-quickstart pycon8

Ci verranno fatte alcune domande necessarie per
configurare il progetto.  Quando ci verrà chiesto
se vogliamo utilizzare ``doctest``, rispondiamo
``y``, mentre per tutto il resto possiamo
lasciare l'opzione di default.  Al termine di
questa operazione, ci ritroveremo una directory
:file:`pycon8` contentente il progetto:

.. code-block:: shell

   $ cd pycon8
   $ ls
   _build  conf.py  index.rst  Makefile  _static  _templates

A questo punto possiamo seguire la presentazione
provando gli esempi in modo autonomo.  Per
portarci nel punto in cui ci troviamo adesso:

.. code-block:: shell

   $ git clone https://github.com/marco-buttu/pycon8.git
   $ git checkout origin/01_create_project
