---
title: "ASD - Powtorzenie do sprawdzianu"
date: 2024-05-09 08:00:00 +0800
categories: [ASD]
tags: [ASD, Definicje, Powtorzenie do sprawdzianu]
---

# Definicje

## Algorytm
Algorytm to dokładny opis czynności przedstawiający jak coś wykonać. Może zostać stworzony jako lista kolejnych kroków.

## Pseudokod
Pseudokod to sposób na zapisanie algorytmu w tak zwanej abstrakcyjnej notakcji, jest on podobny do współczesnych języków programowania takich jak JAVA, Pyhton, C/C++ jednak nie jest żadnym z nich. Pseudokod stanowi rolę informacyjną, a nie formalną.

## Poprawność algorytmów
Poprawne dane wejściowe to takie dane, które spełniają warunek początkowy specyfikacji.

Poprawny wynik algorytmu to taki, który spełnia warunek końcowy specyfikacji.

Algorytm jest całkowicie poprawny wtedy i tylko wtedy, gdy dla każdycch poprawnych danych wejściowych zachodzą oba poniższe warunki:

- Własność stopu - algorytm zatrzymuje się po skończonej liczbie kroków,

- Częściowa poprawność algorytmu - algorytm przy zatrzymaniu zwraca poprawny wynik.

Algorytm jest częściowo poprawny jeśli spełnia warunek w formie implikacji - Jeżeli algorytm zatrzyma się to zwracany jest poprawany wynik. Przy założeniu poprawności danych wejściowych.

## Niezmiennik pętli
Niezmiennik pętli to logiczny predykat spełniający warunek - Jeśli predykat jest spełniony przed wejściem w pewną (Dowolną) iterację pętli to jest także spełniony po wyjściu z tej iteracji pętli.

## Specyfikacja
Specyfikacja to rodzaj "kontraktu" algorytmu, który w sposób bardziej formaly opisuje co dokładnie algorytm ma zrobić. Specyfikacja składa się z następujących części:

- Nazwa algorytmu i następująca po niej lista argumentów w nawiasach (Opcjonalnie).
- Warunek początkowy specyfikujący typy i dopuszczalne wartości poprawnych danych wejściowych.
- Warunek końcowy specyfikujący prawidłowy wynik jego typ i wartość jaki ma być zwrócony przez algorytm jako funkcja danych wejściowych.


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
