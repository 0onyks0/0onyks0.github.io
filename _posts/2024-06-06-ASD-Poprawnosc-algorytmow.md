---
title: "Poprawność algorytmów"
date: 2024-05-09 08:00:00 +0800
categories: [ASD]
tags: [ASD, Poprawność algorytmów]
---

## Definicje
Algorytm - Dokładny opis jak coś wykonać np, jak zaparzyć herbatę. 
Algorytmy są powszechnie stosowane w dziedzinie informatyki.

Pseudokod - Abstrakcyjna metoda podobna do popularnych języków programowania, 
służąca do napisania czynności jakie ma wykonać algorytm.

Specyfikacja - Opisuje co dokładnie ma zrobić algorytm,
jest to rodzaj pewnego kontraktu. W jej skład wchodzi:
- Nazwa algorytmu i następująca po niej lista argumentów w nawiasach (opcjonalnie).
- Warunek początkowy, który specyfikuje typy i dopuszczalne wartości danych wejściowych (wejście).
- Warunek końcowy, który specyfikuje prawidłowy wynik (typ i wartość(i)) 
jaki ma być zwrócony przez algorytm jako funkcja danych wejściowych.

Przykład specyfikacji:
- Nazwa i argumenty - sum(sequence, len).
- Warunek początkowy - sequence - tablica liczb całkowitych, 
len - liczba naturalna będąca deklarowaną długością tablicy.
- Warunek końcowy - algorytm ma zwrócić liczbę całkowitą 
będącą sumą pierwszych len elementów tej tablicy lub zero jeśli jest pusta.

- Całkowicie poprawny algorytm - jest wtedy gdy dla każdych danych wejściowych zachodzą oba warunki:
- Własność stopu - Algorytm zatrzymuje się po skończonej liczbie kroków.
- Częściowa poprawność algorytmu - Algorytm przy zatrzymaniu zwraca poprawny wynik.

Niezmiennik pętli - logiczny predykat spełniający warunek. 
Jeśli predykat jest spełniony przed wejściem w pewną 
iterację pętli to jest także spełniony po wyjściu z tej iteracji pętli.
Niezmienniki są wykorzystywane w udowodnieniu częściowej poprawności algorytmu.
