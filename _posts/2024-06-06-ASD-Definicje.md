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

### Listy dowiązaniowe
Listy dowiązaniowe składają się z węzłów i dowiązań które łączzą węzły. Każdy węzeł jest pewnym kontenerem i przechowuje jeden element. Istnieje wiele wariantów list dowiązaniowych takich jak:
- Jednokierunkowe w których każdy węzeł zawiera wskaźnik do następnego węzła. Oznacza to że w takiej liście można poruszać isę tylko do przodu.
- Dwukierunkowe w których każdy węzeł zawiera wskaźniki do następnika i poprzednika w liście. Dzięki takiemu rozwiązaniu można poruszać się po niej zarówno do przodu i do tyłu.
### Listy dowiązaniowe vs tablice
- tablice:
zalety: bardzo szybki dostęp bezpośredni do dowolnego
elementu, minimalne zużycie pamięci


wady: wstawienie dowolnego elementu w środek ma liniowy
złożoność czasową (przesuwanie innych elementów)
- listy dowiązaniowe:
zalety: wstawienie/usunięcie dowolnie długiej podlisty ma
stałą złożoność czasową, niezależnie od długości podlisty
(wystarczy przestawić stałą liczbę dowiązań)


wady: wolny dostęp do elementów (liniowy) zależący od
miejsca w liście, dodatkowa pamięć na dowiązania
(wskaźniki)

### Abstrakcyjne skrutkury danych
Abstrakcyjna struktura danych zdefiniowana jest przez zestaw operacji, które można wykonać na danych, nie wnikając w ich sposób implementacji. Do takich struktur należy:
- Stos,
- Kolejka,
- Kolejka dwustronna,


### Stabilny algorytm
Algorytm sortujący nazywamy stabilnym wtedy i tylko wtedy, gdy zachowuje pierwotny względny porządek elementów o tej samej warto±ci. np. jeżli ciąg wejściowy zawiera kilka elementów o warto±ci '2', to wszytkie te elementy w ciągu posortowanym będą w takiej samej względnej kolejno±ci:

4, 2a, 3, 1, 2b, 5, 2c -> 1, 2a, 2b, 2c , 3 ,4 ,5

### Kopiec binarny
Kopiec binarny jest binarnym drzewem zupeªnym. Priorytety (wraz z odpowiadaj¡cymi im elementami) trzymane s¡ w w¦zªach drzewa, oraz zachodzi nast¦puj¡cy warunek porz¡dku kopca:

Dla ka»dego w¦zªa, priorytet w tym w¦¹le jest niewi¦kszy, ni» priorytet w w¦zªach potomkach.

### Słownik
Słownik jest abstrakcyjn¡ struktur¡ danych sªu»¡c¡ do operowania na parach klucz-warto±¢.

### Drzewo BST
Drzewo BST jest drzewem binarnym, gdzie ka»dy w¦zeª przechowuje pewien klucz (z przypisan¡ warto±ci¡) i speªniony jest nast¦puj¡cy warunek porz¡dku BST: Dla ka»dego w¦zªa x, klucz w tym w¦¹le jest niemniejszy, ni» wszystkie klucze w lewym poddrzewie w¦zªa x oraz niewi¦kszy, ni» wszystkie klucze w prawym poddrzewie w¦zªa x.

### Drzewo AVL
Drzewo AVL (od nazwisk twórców: Adelson-Velskij, andis) jest drzewem BST z dodatkowym warunkiem. Warunek ten wprowadza dla ka»dego w¦zªa poj¦cie wspóªczynnika zrównowa»enia (bf - od ang. balance factor). Wspóªczynnik zrównowa»enia dla w¦zªa x zdeniowany jest jako ró»nica wysoko±¢i lewego poddrzewa w¦zªa x i prawego poddrzewa w¦zªa x.
Denicja AVL jest nast¦puj¡ca: jest to drzewo BST, które dodatkowo ma wªasno±¢, »e w ka»dym w¦¹le x, bf (x) ∈ {−1, 0, 1}, czyli »e wysoko±ci poddrzew nie mog¡ si¦ ró»ni¢ o wi¦cej ni» 1.

## Metody algorytmów
### Stos
Interfejs stosu (elementów typu Type):
- push(Type e) (dodaj do stosu element e)
- Type pop() (zdejmij i zwró¢ ze stosu element ostatnio dodany - operacja modykuj¡ca)
- Type top() (zwró¢ bez zdejmowania element ostatnio dodany - operacja niemodykuj¡ca)
### Kolejka
Zdeniowana za pomoc¡ nast¦puj¡cego zestawu operacji (interfejsu):
Kolejka (elementów typu Type):
- inject(Type e) (wstaw nowy element do kolejki)
- Type out() (wyjmij i zwró¢ element najdawniej dodany do kolejki - operacja modykuj¡ca)
- Type front() (zwró¢ bez wyjmowania element najdawniej dodany do kolejki - operacja niemodykuj¡ca)
### Kolejka dwustronna
- Type rst() (poka» element z pierwszego ko«ca)
- Type last() (poka» element z drugiego ko«ca)
- pushFront(Type) (dodaj element do pierwszego ko«ca)
- pushBack(Type) (dodaj element do drugiego ko«ca)
- Type popFront() (zwró¢ i zdejmij element z pierwszego ko«ca)
- Type popBack() (zwró¢ i zdejmij element z drugiego ko«ca)
### Kolejka priorytetowa
- insert(e, p) // dodaj element e o priorytecie p do kolejki
- findMin() // // zwró¢ (bez usuwania) element o priorytecie
- najpilniejszym spo±ród przechowywanych obecnie w kolejce
- delMin() // //zwró¢ (z usuwaniem) element j.w.
### Kolej
- insert(e): dodaj nowy element e (wraz z jego priorytetem) w pierwszym od lewej wolnym w¦¹le x ostatniego poziomu, a nast¦pnie przywró¢ porz¡dek kopca pocz¡wszy od w¦zªa x w gór¦ (operacja upheap)
- findMin(): zwró¢ element e znajduj¡cy si¦ w korzeniu kopca
- delMin(): usu« element z korzenia, wstaw do korzenia element ostatni kopca (skrajnie prawy na ostatnim poziomie kopca) i przywró¢ porz¡dek kopca pocz¡wszy od korzenia w dóª (operacja downheap)
### Słownik
- search(K key) (zwraca warto±¢ zwi¡zan¡ z kluczem key)1
- insert(K key, V value) // umieszcza now¡ par¦ klucz-warto±¢ w sªowniku
- delete(K key) // kasuje par¦ zwi¡zan¡ z kluczem key (zakªada si¦, »e klucze s¡ unikatowe

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

### Algorytm wyszukiwania binarnego
```shell
search(S, len, key){
l = 0
r = len - 1
  while(l <= r){
    m = (l + r)/2
      if(S[m] == key) return m
      else
        if(S[m] > key) r = m - 1
        else l = m + 1
  }
return -1
}
```
### Sortowanie przez wybór - selection sort
```shell
selectionSort(S, len){
  i = 0
    while(i < len){
      mini = indexOfMin(S, i, len)
      swap(S, i, mini)
      i++
    }
}
```
### Sortowanie przez wstawienie - insertion sort
```shell
insertionSort(arr, len){
  for(next = 1; next < len; next++){
    curr = next;
    temp = arr[next];
      while((curr > 0) && (temp < arr[curr - 1])){
        arr[curr] = arr[curr - 1];
        curr--;
      }
  arr[curr] = temp;
  }
}
```
### Sortowanie przez zliczanie - count sort
```shell
countSort(a, l){
  max = maxValue(a, l);
  l1 = max + 1;
  counts[l1];
  result[l];
    for(i = 0; i < l1; i++) counts[i] = 0;
      for(i = 0; i < l; i++) counts[a[i]]++;
        for(i = 1; i < l1; i++) counts[i] += counts[i - 1];
          for(i = l - 1; i >= 0; i--)
            result[--counts[a[i]]] = a[i];
}
```
