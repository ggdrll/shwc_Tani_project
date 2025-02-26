# Esame - Data Management Plan


## Sommario esecutivo

1. Analisi quantitativa e qualitativa dei dati attraverso [Voyant Tools](https://voyant-tools.org/).
2. Estrazione dei dati relativi al patrimonio archivistico-librario.
3. Tabellazione dei dati in [Excel](https://www.microsoft.com/it-it/microsoft-365/excel?market=it).
4. Conversione dei dati in formato `.csv`.
5. Pulizia dei dati tramite [Openrefine](https://openrefine.org/).
6. Esportazione dei dati puliti in formato `.csv`.
7. Modellazione in RDF attraverso l'utilizzo di modelli esistenti.


## Introduzione

Il progetto si propone come uno **studio degli elementi di interesse archivistico-librario** contenuti nel testo [Tani A. D. (1922) *Le chiese di Roma: guida storico-artistica. Chiese stazionali*, Edizioni d'arte E. Celanza, Torino](https://archive.org/details/lechiesediromagu00tani/page/n9/mode/2up). 
L'intento complessivo è quello di estrarre dal testo puro dei dati il più possibile allineati con le principali discipline oggetto della classe di laurea LM05, orientando la ricerca verso uno specifico settore delle scienze umanistiche. In particolare, l'idea è quella di **ottenere informazioni strutturate sulle vicende conservative del patrimonio archivistico-librario citato** nella fonte presa in considerazione.


## Descrizione dei dati

I dati raccolti nel progetto provengono da [un'unica fonte](https://github.com/ggdrll/esame/tree/main/docs/fonti): la scansione digitale in formato `.txt` di una guida delle chiese di Roma risalente agli inizi del XX secolo. 

![copertina-Tani](https://www.picclickimg.com/6lwAAOSws9liaRzd/Le-Chiese-Di-Roma-Tani-A-D.webp)

* Il testo sarà sottoposto innanzitutto a un processo di analisi, al fine di comprenderne adeguatamente il contenuto e poter individuare quanti e quali siano i riferimenti relativi ad _archivi_, _biblioteche_, _codici_, _libri_, _documenti_ e _personaggi storici ad essi collegate_.
   * Il processo di analisi verrà presentanto sotto forma di [immagini](https://github.com/ggdrll/esame/tree/main/docs/viz), per offrire una visualizzazione quanto più possibile chiara ed evidente dei dati emersi e dei criteri di ricerca adoperati.

  
* Successivamente, verificata la presenza di aspetti relativi al settore d'interesse, si procederà con l'estrazione dei dati e la loro strutturazione in forma tabellare attraverso Excel. La tabella riporterà:
  * i dati cronotopici relativi alla chiesa a cui appartiene/apparteneva la realtà documentaria;
  * la tipologia di complesso documentario presente (archivio/biblioteca/entrambi);
  * i dati cronotopici relativi al complesso documentario;
  * le informazioni sulle vicende e sulle condizioni conservative del complesso documentario;
  * i dati relativi al contenuto del complesso documentario e ai personaggi storici ad esso collegati.
* I dati modellati in forma tabellare verranno esportati in formato `.csv` per essere puliti tramite Openrefine. La pulizia prevederà:
     * la correzione di eventuali errori grammaticali;
     * la normalizzazione di termini diversi ma relativi alla stessa entità;
     * la riconciliazione di dati a fonti esterne tramite [VIAF](https://viaf.org/en).
 

* Infine, il progetto mirerà a una modellazione dei dati puliti in formato RDF Turtle tramite l'utilizzo di modelli esistenti. I dati codificati in RDF riguarderanno sinteticamente le informazioni di contesto, non la documentazione nello specifico:
   * le chiesa contenente il complesso documentario;
   * la tipologia del complesso documentario;
   * le informazioni sulle vicende e sulle condizioni conservative del complesso documentario.
  



## Documentazione e qualità dei dati

- I dati verranno identificati da identificativi persistenti?
- Quali metadati e documentazione (ad esempio la metodologia di raccolta dei dati e il modo di organizzare i dati) accompagneranno i dati?
- Quali standard verranno utilizzati? Verranno scelti standard per rendere i dati interoperabili?
- Quali misure di controllo della qualità dei dati saranno utilizzate?

## Backup e archiviazione

Durante la ricerca, dati e metadati saranno archiviati e salvati su OneDrive, in locale e all'interno della repository GitHub. La repository sarà articolata secondo la seguente struttura:
* cartella `docs`, contenente il DMP e 2 sottocartelle:
   * `fonti`, all'interno della quale si troveranno l'opera-fonte in formato `.txt` e il dataset originale in formato `.xlsx`;
   * `viz`, all'interno della quale si troveranno le visualizzazioni in formato `.png` e dati ad esse relativi in formato `.xslx`, frutto del processo di analisi preliminare;
* cartella `data`, contente 2 sottocartelle:
   * `csv`, contente i dataset tabellari in formato `.csv` (prima e dopo la pulizia);
   * `rdf`, contente la modellazione dei dati puliti in formato `.ttl`. 

## Requisiti legali ed etici

- Come saranno gestite altre questioni legali, come i diritti di proprietà intellettuale e la proprietà? Quale legislazione si applica?
- Quali questioni etiche e codici di condotta ci sono e come saranno presi in considerazione?

## Condivisione dei dati e conservazione a lungo termine

- I dati saranno condivisi al termine del progetto attraverso l'apertura della repository GitHub e il caricamento su Zenodo.
- I metadati saranno resi disponibili apertamente? Sotto quale licenza saranno pubblicati?
- Come saranno selezionati i dati per la conservazione e dove saranno conservati a lungo termine (ad esempio un repository di dati o un archivio)?
- Quali metodi o strumenti software sono necessari per accedere e utilizzare i dati?
- Come sarà garantita l'applicazione di un identificatore unico e persistente (come un Digital Object Identifier (DOI)) a ciascun set di dati?
