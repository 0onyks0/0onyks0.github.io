---
title: "Złożoność obliczeniowa algorytmów"
date: 2024-05-09 08:00:00 +0800
categories: [ASD]
tags: [ASD, Złożoność obliczeniowa algorytmów]
---

## Definicje
Złożoność czasowa algorytmu - Liczba operacji dominujących
jakie wykona algorytm jako funkcja rozmiaru danych. Mierzy ona jak wiele
pracy musi wykonać algorytm realizujący zadanie w zależności od tego
jak duże są dane. Im niższa złożoność algorytmu tym szybszy jest algorytm.

Operacje dominujące - zbiór operacji, których liczba jest proporcjonalna
do liczby wszystkich operacji wykonywanych przez cały program.
Do operacji dominujących zaliczamy pętle oraz odgałęzienie instrukcji warunkowych.

## Dobry algorytm
Dobry algorytm, który byłby w stanie rozwiązać dany problem
powinien mieć dwie cechy:
- Poprawność - Zwracać prawidłowy wynik, który jest
zgodny z warunkiem końcowym specyfikacji.
Odpowiada to poprawności całkowitej algorytmu.
- Szybkość - Być jak najbardziej wydajny, musi gwarantować
osiągnięcie wyniku przy minimalnym nakładzie zasobów. 
Odpowiada pojęciu złożoności obliczeniowej algorytmu.

## Szybkość algorytmu
Chcąc zmierzyć szybkość algorytmu należy uwzględnić dwa zagadnienia:
- Niezależność od języka programowania / platformy.
- Możliwie duża niezależność od danych wejściowych.
Następnym krokiem będzie zliczenie ilości operacji dominujących.

## Analiza złożoności algorytmu
Przed wykonaniem analizy złożoności algorytmu należy wykonać
dwa kroki:
- Wyznaczyć zbiór operacji dominujących.
- Wyznaczyć funkcję argumentów, która stanowi rozmiar danych wejściowych.

## Przykład

1) Wyznacz operacje dominujące,
2) Wyznacz rozmiar danych.
```shell
find(arr, len, key){
  i = 0
  while(i < len){
    if(arr[i] == key)
    return i
    i++
  }
  return -1
}
```
1) Operacje dominujące:
- Porównanie i < len.
- Porównanie arr[i] == key.
- Zwiększenie indeksu i++.

Są to operacje dominujące, ponieważ wykonują się przez całą pracę programu.
2) Rozmiar danych:
Rozmiar danych stanowi tu długość tablicy arr.
