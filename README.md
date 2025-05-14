Esercizio_1 
# Data Review & Test Planning


Analisi di un dataset contenente informazioni relative a ricevute fiscali. 
Il dataset è stato caricato e analizzato utilizzando Python con libreria Pandas.

## Descrizione del Dataset

Il dataset si compone di quattro campi da analizzare:

- **data**
- **ora**
- **totale**
- **partita iva**

L'obiettivo del progetto è individuare eventuali anomalie nella qualità dei dati.

## Funzioni per l'analisi

Dopo un'iniziale analisi esplorativa del datatset, sono state implementate diverse funzioni per analizzarne e gestirne i dati:

1. **Analisi delle anomalie nella colonna "data"**:
   - Verifica dei valori NaN.
   - Identificazione di formati non conformi, diversi da "00/00/0000".

2. **Analisi delle anomalie nella colonna "ora"**:
   - Verifica dei valori NaN.
   - Identificazione di formati non conformi, diversi da "00:00".

3. **Analisi delle anomalie nella colonna "totale"**:
   - Verifica dei valori NaN.
   - Identificazione di formati non conformi, diversi da "00,00".

4. **Analisi delle anomalie nella colonna "partita iva"**:
   - Verifica dei valori NaN.
   - Identificazione di formati non conformi, diversi da "00000000000".

5. **Conteggio dei valori unici**:
   - Per ciascuna colonna (data, ora, totale, partita iva), viene eseguito il conteggio dei valori unici.

## Come eseguire il codice

Eseguire il codice Python in un ambiente che supporti Pandas.

## Dipendenze

- Python
- Pandas



---


Esercizio_2

# Python Coding: Visualizzazione Geometrica

## Visualizzazione Geometrica OCR ed Entità

Visualizzazione di dati estratti dal file Json su jpg di una ricevuta fiscale.
Gli obiettivi sono visualizzare tutti i **bounding box OCR** sull'immagine (`receipt.jpg`), mostrando anche il testo riconosciuto, e visualizzare i **bounding box delle entità** sovrapposti all’immagine, distinguendoli chiaramente dalle parole OCR. Inoltre utilizzare una codifica visiva per rappresetare il livello di confidenza.

## Descrizione dei Dati

I dati sono strutturati in formato JSON e includono due principali categorie di informazioni:

- **OCR** 
- **Entità**

## Funzionalità dello Script

Dopo aver caricato immagine e dati, lo script `visualization.py` esegue le seguenti operazioni:

## 🔵 Visualizzazione OCR

- Disegno dei **bounding box** per ciascuna parola riconosciuta.
- Visualizzazione del **testo OCR** direttamente sopra il box.

## 🔴 Visualizzazione Entità

- Evidenziazione delle entità estratte tramite **box rossi sfalsati**.
- Visualizzazione del **nome dell'entità** sopra il box.
- Miglioramento (ipotetico) della leggibilità dato da un lieve spostamento delle bounding box e padding visivo.

## **Codifica visiva** in base alla confidenza:
- 🟩 **Verde**: confidenza ≥ 95%
- 🟦 **Blu**: confidenza 80–94%
- 🟥 **Rosso**: confidenza < 80%

## Dipendenze
- Json
- Pillow
- Ipython
