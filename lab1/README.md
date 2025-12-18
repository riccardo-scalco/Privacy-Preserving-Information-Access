# Privacy Preserving Information Access - Homework 1

## Relevance and Anonymization for a Diabetic Dataset

Questo repository contiene lo sviluppo e l'analisi del primo homework per il corso di **Privacy Preserving Information Access** presso l'**Università degli Studi di Padova** (A.A. 2025/2026). Il progetto si concentra sull'applicazione di modelli di anonimizzazione classica per mitigare il rischio di re-identificazione in dataset sensibili.

## 👥 Autori
* **Riccardo Scalco** 
* **Luca Ferrari** 

## 🎯 Obiettivo del Progetto
L'obiettivo è analizzare il livello di privacy di un dataset medico e applicare trasformazioni per soddisfare requisiti di sicurezza standard. Il lavoro esplora il bilanciamento tra la protezione dell'identità dei pazienti e la conservazione dell'utilità del dato per scopi di ricerca epidemiologica.

## 📊 Dataset: Pima Indians Diabetes
L'analisi è condotta sul **Pima Indians Diabetes Database**, focalizzato su pazienti di sesso femminile. 
* **Quasi-Identificatori (QI)**: Attributi come Età, BMI, Numero di Gravidanze e Pressione Sanguigna che, se incrociati con database esterni, possono portare al de-anonimizzazione.
* **Attributi Sensibili**: Livelli di Glucosio, Insulina e l'esito della diagnosi (Outcome).

## 🛠️ Tecniche di Privacy Implementate

### 1. Modelli di Anonimizzazione
* **k-Anonymity**: Trasformazione del dataset affinché ogni individuo non sia distinguibile da almeno altri $k-1$ individui basandosi sui quasi-identificatori.
* **l-Diversity**: Estensione del k-anonimato per garantire che in ogni gruppo di record simili vi sia una sufficiente varietà di valori per gli attributi sensibili, prevenendo attacchi basati sull'omogeneità.
* **t-Closeness**: Rafforzamento della privacy assicurando che la distribuzione di un attributo sensibile in ogni gruppo sia vicina alla distribuzione dell'attributo nell'intero dataset.

### 2. Trasformazione dei Dati
* **Generalizzazione**: Riduzione della granularità dei dati (es. trasformazione dell'età esatta in fasce d'età).
* **Soppressione**: Rimozione di record o attributi troppo specifici (outlier) che facilitano l'identificazione.
* **Microaggregazione**: Sostituzione di valori individuali con valori aggregati (come la media) per gruppi di record simili.

## 📈 Analisi e Risultati
* **Rischio di Re-identificazione**: Valutazione iniziale della percentuale di record univoci nel dataset originale.
* **Utility Loss**: Analisi di quanto le tecniche di anonimizzazione influenzino la correlazione tra le variabili e l'accuratezza delle analisi statistiche successive.
* **Heatmap di Correlazione**: Confronto tra le matrici di correlazione del dataset originale e di quello anonimizzato per misurare la perdita di informazione.

## 💻 Tecnologie Utilizzate
* **Linguaggio**: Python
* **Librerie**: NumPy, Pandas, Matplotlib, Seaborn.
* **Ambiente**: Kaggle Notebook / Jupyter.

## 📂 Struttura del Repository
* `homework-1-ppia.ipynb`: Notebook con l'analisi della vulnerabilità e l'implementazione degli algoritmi di anonimizzazione.
* `homework-1-ppia.pdf`: Relazione tecnica che descrive la metodologia, i criteri di scelta dei quasi-identificatori e i risultati dei test di privacy.
