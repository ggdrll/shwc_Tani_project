# Dataset tabellari

## Indice
1. [Dataset Tani Originale](#dataset-tani-originale)
2. [Dataset Tani Refined](#dataset-tani-refined)

## Dataset Tani Originale

### Nome del file
`datasetTani_og.csv`

### Descrizione
Dataset contenente i dati estratti a seguito del lavoro di analisi svolto con Voyant Tools. Una volta verificata nell'opera l'esistenza di riferimenti ad archivi e biblioteche, i dati in merito sono stati modellati in forma tabellare.

### Struttura
* **Numero di righe**: 11
* **Numero di colonne**: 9
* **Colonne**:
  * `nome_chiesa` : nome della chiesa contenente il complesso documentario;
  * `altri_nomi` : altri nomi con cui è nota la chiesa contenente il complesso documentario;
  * `estremi_cronologici` : data di costruzione e data dell'ultimo intervento apportato all'edificio della chiesa contenente il complesso documentario;
  * `posizione_chiesa` : posizione geografica della chiesa contenente il complesso documentario;
  * `complesso_doc_tipo` : tipologia del complesso documentario contenuto nella chiesa (archivio/biblioteca/entrambi)
  * `complesso_doc_posizione` : posizione ultima del complesso documentario all'interno della chiesa;
  * `complesso_doc_vita` : condizioni ultime e vicende conservative del complesso documentario all'interno della chiesa;
  * `complesso_doc_contenuto` : elementi contenuti nel complesso documentario citati dalla guida;
  * `complesso_doc_personaggi` : personaggi storici legati al complesso documentario.


## Dataset Tani Refined

### Nome del file
`datasetTani_refind.csv`

### Descrizione
Il dataset originale è stato sottoposto a un lavoro di pulizia tramite Openrefine.

### Struttura
* **Numero di righe**: 11
* **Numero di colonne**: 10
* **Colonne**:
  * `nome_chiesa` : nome della chiesa contenente il complesso documentario;
  * `chiesa_id` : URL di riconciliazione della chiesa a fonti esterne; 
  * `altri_nomi` : altri nomi con cui è nota la chiesa contenente il complesso documentario;
  * `estremi_cronologici` : data di costruzione e data dell'ultimo intervento apportato all'edificio della chiesa contenente il complesso documentario;
  * `posizione_chiesa` : posizione geografica della chiesa contenente il complesso documentario;
  * `complesso_doc_tipo` : tipologia del complesso documentario contenuto nella chiesa (archivio/biblioteca/entrambi)
  * `complesso_doc_posizione` : posizione ultima del complesso documentario all'interno della chiesa;
  * `complesso_doc_vita` : condizioni ultime e vicende conservative del complesso documentario all'interno della chiesa;
  * `complesso_doc_contenuto` : elementi contenuti nel complesso documentario citati dalla guida;
  * `complesso_doc_personaggi` : personaggi storici legati al complesso documentario.

