---
title: "ASD - Powtorzenie do sprawdzianu"
date: 2024-05-09 08:00:00 +0800
categories: [ASD]
tags: [ASD, Definicje, Powtorzenie do sprawdzianu]
---

## Definicje

### Algorytm
Algorytm to dokładny opis czynności przedstawiający jak coś wykonać. Może zostać stworzony jako lista kolejnych kroków.

### Pseudokod
Pseudokod to sposób na zapisanie algorytmu w tak zwanej abstrakcyjnej notakcji, jest on podobny do współczesnych języków programowania takich jak JAVA, Pyhton, C/C++ jednak nie jest żadnym z nich. Pseudokod stanowi rolę informacyjną, a nie formalną.

### Poprawność algorytmów
Poprawne dane wejściowe to takie dane, które spełniają warunek początkowy specyfikacji.

Poprawny wynik algorytmu to taki, który spełnia warunek końcowy specyfikacji.

Algorytm jest całkowicie poprawny wtedy i tylko wtedy, gdy dla każdycch poprawnych danych wejściowych zachodzą oba poniższe warunki:

- Własność stopu - algorytm zatrzymuje się po skończonej liczbie kroków,

- Częściowa poprawność algorytmu - algorytm przy zatrzymaniu zwraca poprawny wynik.

Algorytm jest częściowo poprawny jeśli spełnia warunek w formie implikacji - Jeżeli algorytm zatrzyma się to zwracany jest poprawany wynik. Przy założeniu poprawności danych wejściowych.

### Niezmiennik pętli
Niezmiennik pętli to logiczny predykat spełniający warunek - Jeśli predykat jest spełniony przed wejściem w pewną (Dowolną) iterację pętli to jest także spełniony po wyjściu z tej iteracji pętli.

### Specyfikacja
Specyfikacja to rodzaj "kontraktu" algorytmu, który w sposób bardziej formaly opisuje co dokładnie algorytm ma zrobić. Specyfikacja składa się z następujących części:

- Nazwa algorytmu i następująca po niej lista argumentów w nawiasach (Opcjonalnie).
- Warunek początkowy specyfikujący typy i dopuszczalne wartości poprawnych danych wejściowych.
- Warunek końcowy specyfikujący prawidłowy wynik jego typ i wartość jaki ma być zwrócony przez algorytm jako funkcja danych wejściowych.

### Operacje dominujące
Operacje dominujące to te, które proporcjonalnie pokrywają całą pracę algorytmu. Operacją dominującą jest, każda pętla lub odgałęzienie instrukcji warunkowej trwającą przez cały czas do momentu, gdy program się zakończy. Z tego wynika, że operacja wykonana jednokrotnie nie jest operacją dominującą.

### Złożoność czasowa algorytmu
Złożoność czasowa algorytmu to liczba operacji dominujących jakie wykona algorytm jako funkcja rozmiaru danych. Mierzy ona jak wiele pracy musi wykonać algorytm realizujący zadanie w zależności od tego jak duże są dane. Im niższa złożoność algorytmu tym szybszy będzie algorytm. Złożoność czasowa ma dwa warianty:

- Pesymistyczna złożoność czasowa oznaczana jako W() jest to funkcja wyrażająca kres górny możliwej liczby operacji dominujących dla ustalonego rozmiaru danych.
- Przeciętna złożoność czasowa oznaczana jako A() jest to funkcja wyrażająca przeciętną liczbę wykonanych operacji dominujących przy założeniu pewnego modelu losowości danych wejściowych.

### Pamięciowa złożoność algorytmu
Pamięciowa złożoność algorytmu jest to liczba jednostek pamięci głównej użyta przez algorytm jako funkcja rozmiaru danych.

### Notacja "duże o"
Notacja "O()" służy do oznaczania górnego ograniczenia na tempo wzrostu danej funkcji. Notacja O() dla rzędów wielkości funkcji odpowiada intuicyjnie symbolowi ≤ dla liczb.

### Notacja "duże teta"
Notacja "Θ()" służy do wyrażania faktu, że funkcja ma dokładnie taki sam rząd wielkości jak inna funkcja. Odpowiada to więc znakowi “=” dla rzędów wielkości funkcji.

### Dziel i rządź
Dziel i rządź jest jedną z najskuteczniejszych technik projektowania algorytmów. Polega na podzieleniu problemu na podproblemy i wyjaśniamy jak  rozwiązań tych podproblemów otrzymać rozwiązanie oryginalnego problemu.

### Algorytm wyszukiwania binarnego
Algorytm wyszukiwania binarnego:
1. dopóki długość ciągu jest dodatnia:
2. porównaj klucz ze środkowym elementem ciągu,
3. jeżli jest równość, to zwróć wynik (bieżący indeks),
4. jeżli jest niższy niż element - ogranicz dalsze poszukiwania tylko do lewego podciągu (na lewo od bieżącego indeksu),
5. jeżli jest wyższy niż element - ogranicz dalsze poszukiwania tylko do prawego podciągu (na prawo od bieżącego indeksu),
6. wróć do kroku 1,
7 jeżli długość ciągu spadła do zera, to nie ma klucza w ciągu.

## Przykładowe algorytmy

### Algorytm sumowania tablicy

```shell
sum(array[], len) {
  sum = 0
  i = 0
    while(i < len) {
      sum += array[i]
      i++
  }
  return sum
}
```
### Algorytm zwracający maksimum z tablicy

```shell
max(array[], len) {
  i = 1
  x = array[0]
    while(i < len) {
      if(array[i] > x) {
        x = array[i]
      }
      i++
  }
  return x
}
```
### Wyszukiwanie klucza w tablicy

```shell
find(array[], len, key) {
  i = 0
  while(i < len) {
    if(arr[i] == key) {
      return i
    }
  i++
  }
  return -1
}
```
