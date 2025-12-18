# Privacy Preserving Information Access - Progetti A.A. 2025/2026

Questo repository raccoglie il lavoro progettuale svolto per il corso di **Privacy Preserving Information Access** presso l'**Università degli Studi di Padova**. Il percorso esplora le metodologie per l'accesso e l'analisi dei dati garantendo al contempo la protezione della riservatezza dei soggetti coinvolti.

## 👥 Autori
* **Riccardo Scalco** 
* **Luca Ferrari**

## 📁 Struttura del Corso
Il repository è suddiviso in due homework principali che affrontano i due pilastri della protezione dei dati moderni: l'anonimizzazione sintattica e la privacy differenziale.

### 🛡️ Homework 1: Anonimizzazione Sintattica e Rischio di Re-identificazione
Il primo modulo si focalizza sulle tecniche classiche di protezione dei dati per mitigare gli attacchi di re-identificazione.
* **Modelli di Privacy**: Implementazione e analisi di **k-anonymity**, **l-diversity** e **t-closeness**.
* **Trasformazioni**: Applicazione di tecniche di generalizzazione, soppressione e microaggregazione.
* **Analisi del Rischio**: Valutazione della vulnerabilità del dataset originale rispetto a tentativi di de-anonimizzazione tramite quasi-identificatori.

### 📉 Homework 2: Differential Privacy (DP)
Il secondo modulo approfondisce il modello della Privacy Differenziale, considerato lo standard attuale per l'analisi statistica sicura.
* **Meccanismi Implementati**: Sviluppo di algoritmi basati sul rumore di **Laplace**, meccanismo **Esponenziale** e **Randomized Response**.
* **Algoritmi Avanzati**: Implementazione dello **Sparse Vector Algorithm (SVA)** e del protocollo **RAPPOR** di Google.
* **Analisi Utility-Privacy**: Studio del trade-off tra l'accuratezza dei risultati (utilità) e il livello di protezione ($\epsilon$).

## 📊 Dataset di Riferimento
Entrambi i lavori utilizzano il **Pima Indians Diabetes Database**. Questo dataset medico è stato scelto per la sensibilità delle informazioni contenute, rendendolo il candidato ideale per testare l'efficacia delle tecniche di protezione della privacy in ambito epidemiologico.

## 💻 Tecnologie Utilizzate
* **Linguaggio**: Python
* **Librerie**: NumPy, Pandas, Matplotlib, Seaborn.
* **Piattaforme**: Kaggle Notebooks / Jupyter.

## 📂 Contenuto dei Laboratori
Ogni cartella contiene:
1. Il **Notebook (.ipynb)** con l'implementazione del codice e le visualizzazioni grafiche.
2. La **Relazione Tecnica (.pdf)** con l'analisi teorica dei modelli e la discussione dei risultati ottenuti.

---
*Università degli Studi di Padova*
