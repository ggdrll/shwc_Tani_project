# Strangeways, here we come - Vicende conservative di archivi e biblioteche nelle chiese di Roma

## Indice
- [Introduzione](#introduzione)
- [Pianificazione](#pianificazione)
- [Raccolta](#raccolta)
- [Elaborazione e analisi](#elaborazione-e-analisi)
- [Preservazione e condivisione](#preservazione-e-condivisione)
- [Conclusioni](#conclusioni)

----

## Introduzione

Il progetto nasce come prova finale dell'[insegnamento di Digital Humanities e Data Management per i Beni Culturali](https://www.unibo.it/it/studiare/dottorati-master-specializzazioni-e-altra-formazione/insegnamenti/insegnamento/2024/502386). Si è scelto di procedere innanzitutto attraverso un'analisi quantitativa e qualitativa della fonte data dal docente, allo scopo di individuare in essa elementi di interesse archivistico-librario. Una volta presi in considerazione tali elementi, si è voluto procedere con una modellazione dei dati in forma tabellare, così da favorirne la comprensione e la pulizia. Infine, si è ritenuto utile modellare in RDF i dati ottenuti, per garantirne l'interoperabilità e la riusabilità. 
L'intento complessivo è stato quello di estrarre dal testo puro dei dati il più possibile allineati con le principali discipline oggetto del corso di studi LM05, orientando la ricerca verso uno specifico settore delle scienze umanistiche. In particolare, l'idea è stata quella di **ottenere informazioni strutturate sulle vicende conservative del patrimonio archivistico-librario citato nelle fonti prese in considerazione**.

----

## Pianificazione

* In termini di dati, il progetto si è proposto in primis di verificare _la presenza_, all'interno della fonte impiegata, di elementi d'interesse archivistico-librario.
* In particolare, data la natura stessa della guida, si è pianificato di rivolgere l'attenzione soprattutto alle informazioni concernenti _le vicende storico-culturali che avevano coinvolto non tanto le singole chiese, quanto più specificatamente il complesso documentario che esse accoglievano_. Tale requisito è stato definito per far sì che i dati emersi dal progetto potessero risultare effettivamente utili a ricostruire le vicende specifiche dei complessi documentari, e quindi verificare lo stato di conservazione dei materiali in essi contenuti alla data di pubblicazione dell'opera-fonte. Naturalmente, ne è derivata la necessità di puntare a estrarre anche i dati relativi ai singoli elementi contenuti negli archivi e nelle biblioteche citate: ciò ha significato, preliminarmente, individuare all'interno del testo le informazioni relative a libri, codici, manoscritti, documenti di varia natura, nonché alle figure storiche legate ai complessi documentari.
* In definitiva, l'accento è stato posto sui dati relativi alle informazioni di *contesto*, che rappresentano un aspetto fondamentale soprattutto per la disciplina archivistica.

---

## Raccolta

Le dinamiche dietro al processo di analisi dei dati sono state *documentate per immagini* in formato `.png` grazie allo strumento di analisi Voyant Tools. Ciò ha permesso di:
* illustrare la presenza di riferimenti a beni archivistico-librari presenti all'interno dell'opera-fonte, per quanto esigua;
* giustificare la conseguente *raccolta dei dati relativi a tali beni in forma tabellare* (prima in formato `.xslx`, poi convertito in `.csv`).
Nella raccolta, quindi, la scelta è ricaduta sui dati utili a ricostruire le coordinate fisiche e temporali della chiesa e del patrimonio archivistico-librario in essa contenuto. Il formato tabellare è stato scelto per favorire le successive fasi di elaborazione ed analisi, in particolar modo per agevolare la pulizia dei dati stessi e la loro modellazione in altri formati.

---

## Elaborazione e analisi

Una volta creato il dataset tabellare in formato `.csv`, esso è stato sottoposto a un **processo di pulizia** in Openrefine. Gli obiettivi sono stai i seguenti:
* correggere eventuali errori di battitura frutto dell'inserimento manuale dei dati;
* verificare la presenza di termini diversi utilizzati per la stessa entità e normalizzarli;
* riconciliare i dati a fonti esterne tramite VIAF. L'attività di riconciliazione ha coinvolto le chiese e non il patrimonio archivistico-librario specifico per permettere, eventualmente, la successiva integrazione dello stesso dataset attraverso fonti più ampie, più ricche e più aggiornate.

Una volta estratto il dataset tabellare pulito, si è optato per una **modellazione semantica** dei dati relativi alle condizioni e alle vicende dei complessi documentari. 
* Le classi estratte sono le seguenti:
   * Church ;
   * Library ;
   * ArchivalRecordSet .
* Le proprietà estratte sono le seguenti:
   * label ;
   * containsPlace ;
   * description ;
   * type .
* I modelli sono stati tratti da ontologie esistenti quali:
   * [Dublin Core Terms](http://purl.org/dc/terms/);
   * [Schema.org](http://schema.org/);
   * [FaBio](http://purl.org/spar/fabio);
   * [W3C](https://www.w3.org/TR/rdf12-schema/).

---

## Preservazione e condivisione
  
  La scelta di modellazione in RDF Turtle è dettata soprattutto dalla volontà di utilizzare un formato standard che garantisca la disponibilità e l'accesibilità dei dati, così come l'adozione di licenza `CC0 1.0 Universal`. L'intera filiera di raccolta e gestione dei dati è documentata e archiviata in locale, in [OneDrive](https://liveunibo-my.sharepoint.com/my?id=%2Fpersonal%2Fgiulia%5Fguidarelli3%5Fstudio%5Funibo%5Fit%2FDocuments%2Fshwc%5FTani%5Fproject&ga=1) e in repository GitHub con accesso pubblico. Inoltre, i dataset (sia quello tabellare in `.csv` che quello semantico in `.ttl` sono pubblicati su Zenodo e identificati da un DOI: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.14934067.svg)](https://doi.org/10.5281/zenodo.14934067).
  
---

## Conclusioni

I risultati del progetto hanno permesso di mettere in luce la presenza, benché non numerosa, di elementi d'interesse archivistico-biblioteconomico all'interno della guida di Tani. Il progetto potrebbe fungere da base per ulteriori ricerche che permettano di ricostruire, attraverso quanto raccontato nelle guide storico-artistiche, le vicende di complessi documentari che ormai potrebbero essere confluiti all'interno di altre realtà conservative. In sostanza, ha portato a galla _realtà documentarie rimaste quasi "imprigionate" nella narrazione e nelle vicende storico-culturali che le hanno interessate_; attualmente, tuttavia, elementi in origine appartenenti a questi fondi e a questi biblioteche potrebbero essere confluiti in realtà esterne: sarebbe interessante, grazie a quanto avviato con il corrente progetto, poterne ricostruire il percorso conservativo, estendendolo fino ai giorni nostri.
