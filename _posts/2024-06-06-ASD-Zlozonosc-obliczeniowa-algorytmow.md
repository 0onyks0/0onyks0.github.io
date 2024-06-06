---
title: "Złożoność obliczeniowa algorytmów"
date: 2024-05-09 08:00:00 +0800
categories: [ASD]
tags: [ASD, Złożoność obliczeniowa algorytmów]
---

## Definicje
Operacje dominujące - zbiór operacji, których liczba jest proporcjonalna
do liczby wszystkich operacji wykonywanych przez cały program.
Do operacji dominujących zaliczamy pętle oraz odgałęzienie instrukcji warunkowych.

Przykład

Co może być operacją dominującą w poniższym algorytmie?

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
Porównanie i < len.

Porównanie arr[i] == key.

Zwiększenie indeksu i++.

Są to operacje dominujące, ponieważ wykonują się przez całą pracę programu.

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
