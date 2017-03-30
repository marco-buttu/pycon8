Creazione dei contenuti e compilazione
======================================

Come abbiamo appena visto, questa è l'attuale
struttura del progetto:

.. code-block:: shell

   $ cd myproject
   $ ls
   _build  conf.py  index.rst  Makefile  _static

Non abbiamo ancora scritto della documentazione.
L'unico file :file:`rst` è :file:`index.rst`,
creato automaticamente da Sphinx, e questo è il suo
contenuto:

.. code-block:: rst

   ****************************************
   Rules of thumb to test the documentation
   ****************************************

   .. toctree::
      :maxdepth: 2
      :caption: Contents:

Per compilare il progetto e creare la documentazione
in HTML, diamo il comando ``make html``:

.. code-block:: shell

   $ make html

All'interno della directory :file:`_build`
viene creata la directory :file:`html`
contenente la documentazione in formato HTML.

Per poter aggiungere dei nuovi contenuti,
dobbiamo creare dei file :file:`.rst` e
includerli in :file:`index.rst`.  Ad esempio,
se abbiamo creato due file, uno chiamato
:file:`install.rst` e l'altro :file:`build.rst`,
contenenti della documentazione che vogliamo
aggiungere a questo progetto, dobbiamo
includerli in :file:`index.rst` nel seguente modo:

.. code-block:: rst

   ****************************************
   Rules of thumb to test the documentation
   ****************************************

   .. toctree::
      :maxdepth: 2

      install.rst
      build.rst

Per compilare il progetto nel punto in cui ci troviamo
adesso:

.. code-block:: shell

   $ git checkout 02_build_project
   $ make html
