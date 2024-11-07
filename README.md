# MZ zadanie - Analýza sentimentu na Twitteri (X)

Tento projekt vykonáva analýzu sentimentu na dátach z Twitteru pomocou rôznych modelov strojového učenia.

## Požiadavky

- Python 3.x
- Knižnice uvedené v `requirements.txt`

## Inštalácia požadovaných knižníc
Nainštalujte požadované knižnice:
    ```sh
    pip install -r requirements.txt
    ```

## Priebeh

1. Načítanie dát:
    - Tréningové dáta: `data/Twitter/twitter_training.csv`
    - Testovacie dáta: `data/Twitter/twitter_validation.csv`

2. Predspracovanie dát:
    - Odstránenie irelevantných stĺpcov
    - Odstránenie chýbajúcich hodnôt
    - Odstránenie duplikátov
    - Čistenie textu (odstránenie špeciálnych znakov, prevedenie na malé písmo, odstránenie stop slov)
    - Tokenizácia
    - Lematizácia

3. Enkódovanie cieľovej premennej:
    - `Positive` -> 0
    - `Neutral` -> 1
    - `Negative` -> 2
    - `Irrelevant` -> 3

4. Extrakcia príznakov pomocou TF-IDF:
    - Maximálny počet príznakov: 7500

5. Modelovanie:
    - Použité modely: Logistic Regression, Naive Bayes, SVM, Random Forest, Decision Tree, KNN, XGBoost

6. Vyhodnotenie modelov:
    - Výpočet presnosti na testovacích dátach

7. Optimalizácia 3 najlepších modelov pomocou GridSearchCV:
    - Random Forest
    - SVM
    - KNN

8. Generovanie klasifikačných správ a vizualizácia matíc zámen pre najlepšie modely.

## Výsledky

Výsledky modelov sú zobrazené v klasifikačných správach a maticiach zámen.
