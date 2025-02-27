# shwc_tani_project - Data Management Plan

## Indice
* [Sommario esecutivo](#sommarioesecutivo)
* [Introduzione](#introduzione)
* [Descrizione dei dati](#descrizione-dei-dati)
* [Documentazione e qualità dei dati](#documentazione-e-qualità-dei-dati)
* [Backup e archiviazione](#backup-e-archiviazione)

## Sommario esecutivo

1. Analisi quantitativa e qualitativa dei dati attraverso [Voyant Tools](https://voyant-tools.org/).
2. Estrazione dei dati relativi al patrimonio archivistico-librario e tabellazione degli stessi in [Excel](https://www.microsoft.com/it-it/microsoft-365/excel?market=it).
4. Conversione dei dati in formato `.csv`.
5. Pulizia dei dati tramite [Openrefine](https://openrefine.org/).
6. Esportazione dei dati puliti in formato `.csv`.
7. Modellazione in RDF Turtle attraverso l'utilizzo di modelli esistenti.
8. Caricamento dei dataset in formato `.csv` e in formato `.ttl` su [Zenodo](https://zenodo.org/).


## Introduzione

Il progetto si propone come uno **studio degli elementi di interesse archivistico-librario** contenuti nel testo [Tani A. D. (1922) *Le chiese di Roma: guida storico-artistica. Chiese stazionali*, Edizioni d'arte E. Celanza, Torino](https://archive.org/details/lechiesediromagu00tani/page/n9/mode/2up). 
L'intento complessivo è quello di estrarre dal testo puro dei dati il più possibile allineati con le principali discipline oggetto della classe di laurea LM05, orientando la ricerca verso uno specifico settore delle scienze umanistiche. In particolare, l'idea è quella di **ottenere informazioni strutturate sulle vicende conservative del patrimonio archivistico-librario citato** nella fonte presa in considerazione.


## Descrizione dei dati

I dati raccolti nel progetto provengono dalla scansione digitale in formato `.txt` di una guida delle chiese di Roma risalente agli inizi del XX secolo. 

![copertina-Tani](https://www.picclickimg.com/6lwAAOSws9liaRzd/Le-Chiese-Di-Roma-Tani-A-D.webp)

* Il testo sarà sottoposto innanzitutto a un processo di analisi, al fine di comprenderne adeguatamente il contenuto e poter individuare quanti e quali siano i riferimenti relativi ad _archivi_, _biblioteche_, _codici_, _libri_, _documenti_ e _personaggi storici collegati ai complessi documentari citati_.
   * Il processo di analisi verrà presentanto sotto forma di [immagini](https://github.com/ggdrll/esame/tree/main/docs/viz), per offrire una visualizzazione quanto più possibile chiara ed evidente dei dati emersi e dei criteri di ricerca adoperati.

  
* Successivamente, verificata la presenza di aspetti relativi al settore d'interesse, si procederà con l'estrazione dei dati e la loro [strutturazione in forma tabellare](https://github.com/ggdrll/shwc_Tani_project/blob/main/docs/fonti/datasetTani_og.xlsx) attraverso Excel. La tabella riporterà:
  * i dati cronotopici relativi alla chiesa a cui appartiene/apparteneva la realtà documentaria;
  * la tipologia di complesso documentario presente (archivio/biblioteca/entrambi);
  * i dati cronotopici relativi al complesso documentario;
  * le informazioni sulle vicende e sulle condizioni conservative del complesso documentario;
  * i dati relativi al contenuto del complesso documentario e ai personaggi storici ad esso collegati.
* I dati modellati in forma tabellare verranno [esportati in formato `.csv`](https://github.com/ggdrll/shwc_Tani_project/blob/main/data/csv/datasetTani_og.csv) per essere [puliti](https://github.com/ggdrll/shwc_Tani_project/blob/main/data/csv/datasetTani_refined.csv) tramite Openrefine. La pulizia prevederà:
     * la correzione di eventuali errori grammaticali;
     * la normalizzazione di termini diversi ma relativi alla stessa entità;
     * la riconciliazione di dati a fonti esterne tramite [VIAF](https://viaf.org/en).
 

* Infine, il progetto mirerà a una [modellazione](https://github.com/ggdrll/shwc_Tani_project/tree/main/data/rdf) dei dati puliti in formato RDF Turtle tramite l'utilizzo di ontologie esistenti per garantire l'interoperabilità. I dati codificati in RDF riguarderanno sinteticamente le informazioni di contesto, non la documentazione nello specifico, ossia:
   * le chiesa contenente il complesso documentario;
   * la tipologia del complesso documentario contenuto nella chiesa;
   * le informazioni sulle vicende e sulle condizioni conservative del complesso documentario.
  

## Documentazione e qualità dei dati

Il dataset in formato tabellare e il dataset semantico verranno identificati da un DOI assegnato attraverso il caricamento degli stessi su Zenodo. 
I dati saranno di volta in volta descritti all'interno dei file README.md presenti in ogni cartella e sottocartella della repository; inoltre, i rimandi interni nella struttura della repository aiuteranno a seguire la loro filiera di raccolta e gestione.
La scelta di formati come `.csv` e `.ttl` mira all'interoperabilità e al riuso dei dataset, così come la scelta della licenza `CC0 1.0 Universal`.


## Backup e archiviazione

Durante la ricerca, dati e metadati saranno archiviati e salvati su [OneDrive](https://liveunibo-my.sharepoint.com/:f:/g/personal/giulia_guidarelli3_studio_unibo_it/EvJFrbOEb19Jsbj3MTFjx3sB-jsAwoOrGzGj5pYHi0qaug?e=QkbzfH), in locale e all'interno della repository GitHub. La repository sarà articolata secondo la seguente struttura:
* cartella `docs`, contenente il DMP e 2 sottocartelle:
   * `fonti`, all'interno della quale si troveranno l'opera-fonte in formato `.txt` e il dataset originale in formato `.xlsx`;
   * `viz`, all'interno della quale si troveranno le visualizzazioni in formato `.png` e dati ad esse relativi in formato `.xslx`, frutto del processo di analisi preliminare;
* cartella `data`, contente 2 sottocartelle:
   * `csv`, contente i dataset tabellari in formato `.csv` (prima e dopo la pulizia);
   * `rdf`, contente la modellazione dei dati puliti in formato `.ttl`. 
