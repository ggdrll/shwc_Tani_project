# Titolo del progetto

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
L'intento complessivo è quello di estrarre dal testo puro dei dati il più possibile allineati con le principali discipline oggetto del corso di studi LM05, orientando la ricerca verso uno specifico settore delle scienze umanistiche. In particolare, l'idea è quella di **ottenere informazioni strutturate sulle vicende conservative del patrimonio archivistico-librario citato nelle fonti prese in considerazione**.

----

## Pianificazione

* In termini di dati, il progetto si è proposto in primis di verificare _la presenza_, all'interno della fonte impiegata, di elementi d'interesse archivistico-librario.
* In particolare, data la natura stessa della guida, si è pianificato di rivolgere l'attenzione soprattutto alle informazioni concernenti _le vicende storico-culturali che avevano coinvolto non tanto le singole chiese, quanto più specificatamente il complesso documentario che esse accoglievano_. Tale requisito è stato definito per far sì che i dati emersi dal progetto potessero risultare effettivamente utili a ricostruire le vicende specifiche dei complessi documentari, e quindi verificare lo stato di conservazione dei materiali in essi contenuti alla data di pubblicazione dell'opera-fonte. Naturalmente, ne è derivata la necessità di puntare a estrarre anche i dati relativi ai singoli elementi contenuti negli archivi e nelle biblioteche citate: ciò ha significato, preliminarmente, individuare all'interno del testo le informazioni relative a libri, codici, manoscritti, documenti di varia natura, nonché alle figure storiche legate ai complessi documentari.
* In definitiva, nel processo di selezione dei dati, l'accento è stato posto sulle informazioni di *contesto*, che rappresentano un aspetto fondamentale soprattutto per la disciplina archivistica.

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

Una volta estratto il dataset pulito, si è optato per una **modellazione in RDF Turtle**. 

---

## Preservazione e condivisione

I dati sono stati salvati sia in locale sia in OneDrive prima di essere caricati su repository in GitHub. La repository è articolata secondo la seguente struttura:
* cartella docs, contenente il DMP e 2 sottocartelle:
   * fonti, all'interno della quale si trovano l'opera-fonte in formato .txt e il dataset originale in formato .xlsx;
   * viz, all'interno della quale si trovano le visualizzazioni frutto del processo di analisi preliminare;
* cartella data, contente 2 sottocartelle:
   * csv, contente i dataset tabellari in formato .csv (prima e dopo la pulizia);
   * rdf, contente la modellazione dei dati puliti in formato .ttl. 
  
  Per garantirne l'integrità, la disponibilità e l'accesibilità a lungo termine, formati, Zenodo, licenza libera.
  
---

## Conclusioni

In questa sezione, riassumi i principali risultati del progetto e rifletti su eventuali sfide o lezioni apprese durante il processo di gestione dei dati. GROSSE SFIDE SEB
