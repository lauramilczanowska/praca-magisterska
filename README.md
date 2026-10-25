# 📉 Rola horyzontu czasowego w prognozowaniu upadłości przedsiębiorstw

W repozytorium znajduje się **wyłącznie rozdział 3 – część empiryczna** pracy magisterskiej. Pozostałe rozdziały nie zostały tu zamieszczone.

📎 **[Rozdział 3 w formacie PDF](/rozdział3.pdf)**

## 🎯 Cel badania

Sprawdzenie, jak **horyzont prognozy** (liczba lat dzielących moment oceny od upadłości) wpływa na skuteczność modeli przewidujących upadłość przedsiębiorstw. W rozdziale porównano modele budowane dla różnych horyzontów czasowych: 1 - 5 lat przed upadłością.

## 🗂️ Dane

- **Źródło:** [[polish companies bankruptcy data](https://archive.ics.uci.edu/dataset/365/polish+companies+bankruptcy+data)]
- **Próba:** łącznie 43 004 przedsiębiorstwa
- **Okres:** firmy, które zbankrutowały, analizowano w latach 2000-2012, natomiast firmy nadal funkcjonujące badano w okresie 2007-2013. 
- **Zmienne:** 64 wskaźniki finansowe

## 🔬 Metodyka

1. Przygotowanie danych i wstępna analiza
2. Wybór zmiennych objaśniających: wskaźnik IV (Information Value), Random Forest, średnia ranga isotności korelacja Spearmana
3. Budowa modeli dla poszczególnych horyzontów: regresja logistyczna
4. Ocena jakości modeli: AUC, ACC, czułość, specyficzność, NPV, PPV, test Hosmera - Lemeshowa

## 📊 Wyniki

Model 1 zbudowano na danych z pierwszego roku okresu prognozowania, pięć lat przed 
wystąpieniem zdarzenia i jest to najdłuższy badany horyzont czasowy.

| Model | AUC | ACC | Czułość | Specyficzność |
| :--- | :---: | :---: | :---: | :---: |
| Model 1 | 0,850 | 0,781 | 0,779 | 0,781 |
| Model 2 | 0,805 | 0,720 | 0,726 | 0,720 |
| Model 3 | 0,818 | 0,741 | 0,736 | 0,741 |
| Model 4 | 0,810 | 0,737 | 0,741 | 0,736 |
| Model 5 | 0,882 | 0,810 | 0,811 | 0,810 |

**Najważniejsze wnioski:**
- Najwyższą skutecznością predykcyjną charakteryzował się model oparty na danych z roku bezpośrednio 
poprzedzającego bankructwo, co jest wynikiem zgodnym z oczekiwaniami.
- Kluczowym i nieoczekiwanym wynikiem badania jest brak monotonicznego trendu wzrostowego skuteczności wraz ze skracaniem horyzontu. Lepsze wyniki modelu z 5-letnim horyzontem niż 4-letnim, może wynikać z różnic w składzie i liczebności prób lub ze specyfiki okresu obserwacji i wymaga pogłębionej analizy w przyszłych badaniach.

## 🛠️ Narzędzia

- **STATISTICA** – analiza danych i budowa modeli
- Excel
