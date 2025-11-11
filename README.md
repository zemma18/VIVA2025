# GBV & Survivor

Il progetto di ricerca  VIVA, vinto all'interno della progettualità annuale del Dipartimento di Studi Umanistici,Università IULM MILANO, propone un modo alternativo per  generare  dati testuali e al contempo contribuire all'individuazione dei pattern che definiscono i percorsi uscita dalla spirale della violenza di genere. Altro obiettivo della ricerca è colmare il gap sulla disponibilità di dati sulla tematica.

VIVA analizza le storie delle sopravvissute per definire scenari futuri e strategie di comunicazione al fine di identificare best practices per riconoscere in anticipo situaizoni di potenziale disagioo pericolo. 
# GBV & Survivor: Dataset

## Descrizione generale
Questo dataset raccoglie e analizza casi di **violenza di genere** riportati in contesti diversi (es. lavorativi, istituzionali, familiari).  
Il corpus è basato su estratti di storie di sopravvissute tratte da fonti giornalistiche e televisive, trasformati da audio a testo, sottoposti a un processo di pre-trattamento testuale ed elaborati con tecniche di NLP.
Ogni record documenta un episodio, con informazioni testuali e metriche derivate da analisi semantiche e di sentiment.  

L’obiettivo è supportare la ricerca sulla **prevenzione della violenza di genere**, partendo dalle narrazioni dei percorsi di uscita dalla spirale di violenza per arrivare all'individuaizione esatto del punto della spirale in cui si trova l'individuo destinatario delel diverse forme violenze. Il data base è da usare come uno strumento oreintativo per una autovalutaizone della sua posizione all'interno della spirale di violenza.



## Struttura del dataset

| Colonna | Descrizione |
|----------|-------------|
| **doc_id** | Identificativo univoco del documento o caso. |
| **Tipo di violenza** | Tipologie di abuso rilevate (es. molestie sessuali, psicologiche, mobbing, abuso di potere). |
| **Genere vittima** | Genere della vittima coinvolta. |
| **Abusante** | Ruolo o categoria dell’abusante (es. colleghi, superiori, partner). |
| **Esito** | Conseguenze o esiti legali/sociali del caso. |
| **Azione/i preventiva/e della vittima** | Strategie o azioni messe in atto dalla vittima (es. denuncia, richiesta di trasferimento). |
| **Cluster_tematico** | Tre principali livelli di autovalutazione della spirale di violenza  |
| **sentiment medio** | Valore medio di sentiment dell’intero testo (negativo < 0 < positivo). |
| **dev. sd. sentiment** | Deviazione standard del sentiment (indicatore di variabilità emotiva). |
| **parola positiva** | Termine con connotazione positiva più significativa nel testo. |
| **sentiment parola positiva** | Valore di sentiment associato alla parola positiva. |
| **parola neutra** | Termine neutro rilevante nel contesto. |
| **sentiment parola neutra** | Valore di sentiment associato alla parola neutra. |
| **parola negativa** | Termine con connotazione negativa più significativa nel testo. |
| **sentiment parola negativa** | Valore di sentiment associato alla parola negativa. |

---

## Esempio di record

| doc_id | Tipo di violenza | Genere vittima | Abusante | Esito | Azione/i preventiva/e della vittima | Cluster_tematico | sentiment medio | dev. sd. sentiment | parola positiva | sentiment parola positiva | parola neutra | sentiment parola neutra | parola negativa | sentiment parola negativa |
|---------|------------------|----------------|-----------|--------|-----------------------------------|------------------|------------------|---------------------|----------------|----------------------------|----------------|--------------------------|----------------|----------------------------|
| 2018_1 | molestie sessuali sul posto di lavoro, molestie psicologiche, mobbing e abuso di potere | donna | vertici sezione militare, colleghi | condanna blanda dell’abusante, pensionamento anticipato | denuncia, resistenza, richiesta di trasferimento | Exit from violence / Rebirth | -0,535 | 0,279 | personalità_affascinante | 0,34 | situazione_contraddittoria | 0 | manipolatore_pericoloso | -0,78 |

---

## Note metodologiche
- L’analisi del sentiment è stata effettuata su testi in lingua italiana confrontando diversi algoritmi .  
- Le parole chiave (positive, neutre, negative) derivano da una combinazione di lessici semantici e embedding contestuali.  
- I cluster tematici sono stati ottenuti tramite **analisi semantico-topica** (Embedding Topic Modeling).  
- Tutti i dati sono **anonimizzati** e destinati esclusivamente a fini di ricerca.

---

## Licenza
Questo dataset è rilasciato sotto licenza **CC BY 4.0** (Creative Commons Attribution 4.0 International).  
Può essere riutilizzato e citato con attribuzione all’autore.

---
## Team di Ricerca:
-  Emma ZAVARRONE (Responsabile)
- Alessia Forciniti
- Elisa Pasino
  
--
## Citazione
Se utilizzi questo dataset, cita come:
Zavarrone E and Forciniti A. (2025). *GBV & Survivor: Dataset (v1.0)*. GitHub.
 https://github.com/zemma18/violenza-genere-dataset

 Con riferimento all'uso delle fonti su cui si basa la costruzioine del dataset, si segnala che:
 - l'art.64 sexies della L. 633/41 che esclude la necessità di autorizzazione del proprietario del database per l'accesso e la consultazione dei contenuti ivi riportati quando "abbiano esclusivamente finalità didattiche o di ricerca scientifica, non svolta nell'ambito di un'impresa, purché si indichi la fonte e nei limiti di quanto giustificato dallo scopo non commerciale perseguito";
 
- l'art 70 ter 3 co. 1 della L. 633/41 che consente "le riproduzioni compiute da organismi di ricerca e da istituti di tutela del patrimonio culturale, per scopi di ricerca scientifica, ai fini dell'estrazione di testo e di dati da opere o da altri materiali disponibili in reti o banche di dati cui essi hanno lecitamente accesso, nonché la comunicazione al pubblico degli esiti della ricerca ove espressi in nuove opere originali" e il co. 4 che stabilisce chiaramente che "(...) per organismi di ricerca si intendono le università (...)".


