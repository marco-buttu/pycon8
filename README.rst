Abstract
--------

Nel lontano 1999 Tim Peters fece alcune `considerazioni
<https://groups.google.com/forum/#!msg/comp.lang.python/DfzH5Nrt05E/Yyd3s7fPVxwJ>`_
in merito alla documentazione del codice. Scrisse che gli esempi non hanno prezzo,
che gli esempi che non funzionano sono peggio di quelli inutili, e che gli esempi
che funzionano alla fine diventano esempi che non funzionano.  Queste sostanzialmente
furono le motivazioni che lo spinsero a scrivere il modulo `doctest
<https://docs.python.org/3/library/doctest.html>`_ della libreria standard.  Da quel
momento nel mondo Python si è iniziato a prestare particolare attenzione ai test della
documentazione.  Non abbastanza però. Si pensi che attualmente (inizio 2017), la
documentazione ufficiale di Python conta circa 450 failures su 2100 test complessivi.
Questi fallimenti sono dovuti solo in minima parte ad esempi errati. Generalmente
(ma anche in questo caso specifico) le cause sono la mancanza di isolamento tra i test,
assieme alla scarsa dimestichezza con il framework di test.  Entrambe le cause possono
portare a brutte sorprese, come ad esempio dei test ballerini, che a volte passano e a
volte no, senza apparente motivo.  Lo scopo di questo talk è quindi mostrare come
scrivere correttamente gli esempi ed il codice presenti nella documentazione (doc utente,
tutorial, docstring, libri, o altro), in modo da tenere sotto controllo la situazione
ed evitare spiacevoli sorprese e perdite di tempo.

`Marco Buttu @ PyCon Italia 8
<https://www.pycon.it/conference/talks/rules-of-thumb-to-test-the-documentation>`_,
Firenze, 6-9 aprile 2017.

Materiale: `<https://github.com/marco-buttu/pycon8>`_.
