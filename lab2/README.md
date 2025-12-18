# Privacy Preserving Information Access - Homework 2

## Differential Privacy on a Diabetic Dataset

Questo repository contiene lo sviluppo e l'analisi del secondo homework per il corso di **Privacy Preserving Information Access** presso l'**Università degli Studi di Padova** (A.A. 2025/2026). Il progetto esplora l'applicazione pratica della **Differential Privacy (DP)** su dati medici sensibili.

## 👥 Autori
* **Riccardo Scalco** 
* **Luca Ferrari**

## 🎯 Obiettivo del Progetto
L'obiettivo è proteggere la privacy dei pazienti all'interno di un dataset sanitario, mantenendo al contempo l'utilità statistica per query e analisi. Sono stati implementati diversi algoritmi di Differential Privacy per valutare il trade-off tra protezione dei dati (budget di privacy $\epsilon$) e accuratezza dei risultati.

## 📊 Dataset: Pima Indians Diabetes
Il dataset analizzato è il **Pima Indians Diabetes Database**, che include record medici di circa 800 pazienti:
* **Attributi**: BMI, livello di glucosio, pressione sanguigna, età, gravidanze, ecc.
* **Quasi-Identificatori**: Gli attributi medici, se combinati, possono identificare univocamente un individuo.
* **Target**: Variabile binaria che indica la presenza di diabete.



## 🛠️ Tecniche Implementate

### 1. Meccanismi di Base
* **Randomized Response (Coin Toss)**: Utilizzo del lancio della moneta (standard ed $\epsilon$-biased) per fornire negazione plausibile su risposte binarie.
* **Meccanismo di Laplace**: Aggiunta di rumore calibrato sulla sensibilità delle query per rendere sicuri gli istogrammi e i conteggi delle feature mediche.

### 2. Algoritmi Avanzati
* **Meccanismo Esponenziale**: Selezione del valore ottimale (es. la fascia d'età più frequente) preservando la privacy tramite una funzione di utilità.
* **Sparse Vector Algorithm (SVA)**: Implementazione di SVA (standard e numerico) per rispondere a query che superano una determinata soglia, ottimizzando il consumo del budget di privacy.
* **RAPPOR (Google's Protocol)**: Implementazione del protocollo *Randomized Aggregatable Privacy-Preserving Ordinal Response* per la raccolta di statistiche aggregate in modo anonimo, con un'analisi del budget fissata a $\epsilon \approx 0.95$.

## 📈 Analisi dei Risultati
* **Utilità dei Dati**: I grafici comparativi dimostrano che, nonostante l'inserimento di rumore, le distribuzioni delle feature (come il BMI o l'età) rimangono statisticamente significative per l'analisi medica.
* **Privacy Budget**: Il lavoro analizza come la variazione di $\epsilon$ influenzi la distorsione dei dati, identificando i parametri ottimali per bilanciare sicurezza e precisione.

## 💻 Tecnologie Utilizzate
* **Linguaggio**: Python
* **Librerie**: NumPy, Pandas, Matplotlib, Seaborn.
* **Ambiente**: Kaggle Notebook / Google Colab.

## 📂 Struttura del Repository
* `homework-2-ppia.ipynb`: Notebook completo con codice, simulazioni e visualizzazioni.
* `homework-2-ppia.pdf`: Relazione tecnica con approfondimenti teorici e interpretazione dei grafici.
