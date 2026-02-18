link do Power BI ---> https://1drv.ms/f/c/bf2707aa6b084d0d/IgCJzCueweeeSKUGKPo_6GhqAVENQgnWLd9VhiRouwWz7f0?e=SK0Cce

Celem projektu była analiza opinii klientów pod kątem:

rozkładu sentymentu (pozytywny / negatywny),

jakości klasyfikacji (confidence score),

źródeł opinii,

zmian liczby opinii w czasie.

Projekt został zrealizowany z wykorzystaniem:

Oracle SQL

Python (pandas, matplotlib)

Power BI


Analiza w SQL (Oracle)

W bazie danych przeprowadzono eksplorację i agregację danych:

Eksploracja danych

sprawdzenie struktury tabeli (SELECT *)

zliczenie liczby rekordów (COUNT(*))

podgląd próbki danych (FETCH FIRST 5 ROWS ONLY)

Analiza sentymentu

zliczenie opinii według sentymentu (GROUP BY SENTIMENT)

filtrowanie opinii pozytywnych (WHERE SENTIMENT = 'Positive')

ranking opinii według confidence score (ORDER BY CONFIDENCE_SCORE DESC)

Analiza tekstu

wyszukiwanie słów kluczowych w treści opinii (LIKE, LOWER())

Analiza w czasie

agregacja liczby opinii według daty (TRUNC(CREATED_AT))

Statystyki jakości

wyznaczenie minimalnego i maksymalnego confidence score


PYTHON
Dane zostały poddane dodatkowej analizie eksploracyjnej:

Przygotowanie danych

wczytanie danych z pliku CSV

analiza struktury danych (info())

statystyki opisowe (describe())

identyfikacja i usunięcie braków danych

Transformacje

filtrowanie opinii pozytywnych

utworzenie zmiennej logicznej HIGH_CONFIDENCE (confidence > 0.8)

Agregacja

obliczenie średniego confidence score dla każdego sentymentu

Wizualizacja

histogram rozkładu confidence score



Na podstawie danych przygotowano dashboard:

Główne wskaźniki:

liczba opinii

procent opinii pozytywnych

procent opinii negatywnych

średni confidence score

udział opinii o wysokim poziomie pewności

Wizualizacje:

liczba opinii wg sentymentu

średni confidence wg sentymentu

liczba opinii wg źródła
