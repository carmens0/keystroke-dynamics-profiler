# Keystroke Dynamics Profiling

## Descrizione del Progetto
Questo progetto esplora l'uso della **keystroke dynamics** per la profilazione dell'utente, identificando attributi come la **lingua parlata**, la **provenienza geografica** e l'**esperienza con la dattilografia**. Utilizzando tecniche di **machine learning**, il progetto analizza dati biometrici comportamentali estratti dalla digitazione per migliorare la classificazione demografica.

## Contesto
La **keystroke dynamics** è un campo interdisciplinare che combina **biometria, cibernetica e psicologia cognitiva**. Studia il comportamento di digitazione degli utenti attraverso metriche come:
- **Velocità di battitura**
- **Intervallo tra pressioni di tasti (IKI)**
- **Durata della pressione dei tasti**
- **Tasso di errore**

Queste informazioni possono essere utilizzate per **autenticazione utente** o per **profilazione demografica**, senza richiedere hardware specializzato.

## Dataset
Il progetto utilizza il dataset **"136M keystrokes"**, un set di dati pubblico con:
- **169,000 utenti**
- **16 variabili principali**, tra cui ID utente, tempo di pressione dei tasti, lingua parlata e layout di tastiera
- **Dati demografici** come genere, età e nazione di origine

I dati sono stati puliti ed elaborati tramite **data wrangling**, con operazioni come:
- Gestione dei **missing values**
- Individuazione di **outlier** (es. età superiore a 120 anni)
- Creazione di nuove feature (es. **diagraphs** e **rollover ratio**)

## Metodologia
L'analisi si basa su un **protocollo sperimentale** con 3 fasi principali:
1. **Feature Engineering**: estrazione di metriche significative dalla digitazione
2. **Training e Valutazione**: utilizzo di **7 modelli di Machine Learning**, tra cui:
   - **Random Forest**
   - **Gradient Boosting**
   - **XGBoost**
   - **MLP (Neural Network)**
3. **Gestione del Bilanciamento**: implementazione di **SMOTE** e tecniche di **folding** per gestire dataset sbilanciati

## Risultati Principali
Dopo numerosi esperimenti, i modelli migliori per ogni task sono:
| Task | Categorie | Miglior Modello | Accuratezza |
|------|----------|----------------|-------------|
| **Area Geografica** | America / Non-America | Gradient Boosting (SMOTE) | **77%** |
| **Lingua Parlata** | Inglese / Non-Inglese | Gradient Boosting (SMOTE) | **88%** |
| **Corso di Scrittura** | Sì / No | Gradient Boosting (SMOTE) | **75%** |

I task su **genere** e **età** hanno mostrato difficoltà maggiori, probabilmente a causa della **sovrapposizione di pattern di digitazione**.

## Installazione e Utilizzo
### Prerequisiti
- Python >= 3.8
- Librerie richieste: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `seaborn`, `matplotlib`

### Installazione
```bash
pip install -r requirements.txt
```

### Esecuzione del Codice
```bash
python main.py
```

## Possibili Applicazioni
- **Autenticazione Utente**: utilizzo della digitazione come firma biometrica
- **Analisi Demografica**: studio di pattern linguistici e geografici
- **Personalizzazione UX**: adattamento di interfacce in base alla digitazione dell'utente

## Autori

## Author and contact 

| Name                | Description                                                                                       |
|---------------------|---------------------------------------------------------------------------------------------------|
| **Carmela Pia Senatore** | Developer - [carmens0](https://github.com/carmens0) <br> Email - [carmensenatore58@gmail.com](mailto:carmensenatore58@gmail.com) <br> LinkedIn - [Carmela Pia Senatore](https://linkedin.com/in/carmela-pia-senatore-ba1797207) |
| **Gennaro Capaldo**  | Developer - [gennaroc01](https://github.com/Gennaroc01) <br> Email - [gennaro.capaldo2001@gmail.com](mailto:gennaro.capaldo2001@gmail.com) <br> LinkedIn - []() |


## Contatti
Per domande o collaborazioni, contattaci.

