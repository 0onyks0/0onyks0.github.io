---
title: "Linux Firewall"
date: 2024-05-09 08:00:00 +0800
categories: [Linux]
tags: [Linux, Firewall, Security]
layout: post
---

<h2>Wprowadzenie</h2>
Po utworzeniu nowego serwera opartego na Debianie lub Ubuntu, kluczowym krokiem jest skonfigurowanie zaporę ogniowej. To filtrowanie ruchu sieciowego, kontrolujące przychodzące i wychodzące połączenia. Dzięki ustawianiu reguł, możemy kontrolować, które połączenia są dozwolone, co zwiększa bezpieczeństwo serwera poprzez blokowanie nieautoryzowanych prób dostępu oraz ataków sieciowych. Skonfigurowanie zaporę na wczesnym etapie zapewnia bezpieczeństwo i kontrolę nad ruchem sieciowym.

<h2>Instalacja zapory</h2>
W przypadku serwerów opartych na Debianie oraz Ubuntu, zapory sieciowe mogą być używane do kontrolowania, które połączenia z określonymi usługami są dozwolone. W tym przewodniku skoncentrujemy się na instalacji i użyciu zapory UFW (Uncomplicated Firewall), która pomaga w ustawieniu reguł zapory i zarządzaniu wyjątkami.

Aby zainstalować UFW, możemy skorzystać z menedżera pakietów. Najpierw należy zaktualizować lokalny indeks pakietów, aby uzyskać najnowsze informacje o dostępnych pakietach:

```shell
sudo apt update
```

Po aktualizacji lokalnego indeksu pakietów możemy przejść do instalacji zapory:

```shell
sudo apt install ufw
```

Po zainstalowaniu zapora pozostaje wyłączona do momentu, aż sami ją uruchomimy wydając komendę:

```shell
sudo ufw enable
```

<h2>Profile aplikacji:</h2>
Profile zapory w UFW umożliwiają zarządzanie nazwanymi zestawami reguł zapory dla zainstalowanych aplikacji. UFW dostarcza domyślne profile dla wielu popularnych programów, a także pozwala na rejestrowanie dodatkowych profili podczas instalacji pakietów. Na przykład, OpenSSH, usługa, która umożliwia połączenie się z serwerem, ma swój własny profil zapory, który możemy wykorzystać. Warto jednak pamiętać o tym, że opcja profili obsługuje tylko domyślne porty. Gdy zmienimy domyślny port usługi to trzeba również ręcznie dodać zmieniony port.

<h2>Podstawowe komendy</h2>

Wyświetlenie dostępnych profili zapory:

```shell
sudo ufw app list
```

Zezwolenie na połączenie profilowi:

```shell
sudo ufw allow <Nazwa_profilu>
```

Wyłączanie zapory UFW:

```shell
sudo ufw disable
```

Sprawdzanie statusu zapory UFW:

```shell
sudo ufw status
```

Dodawanie reguł:

```shell
sudo ufw allow <port>/<protokół>
```

Usuwanie reguł:

```shell
sudo ufw delete allow <port>/<protokół>
```

Zezwolenie na połączenia z konkretnego adresu IP:

```shell
sudo ufw allow from <adres_IP>
```

Zablokowanie połączeń z konkretnego adresu IP:

```shell
sudo ufw deny from <adres_IP>
```

Zezwolenie na połączenia z określonej podsieci IP:

```shell
sudo ufw allow from <adres_IP>/<maska_podsieci>
```

Zablokowanie połączeń z określonej podsieci IP:

```shell
sudo ufw deny from <adres_IP>/<maska_podsieci>
```

Zezwolenie na konkretny port z określonego adresu IP:

```shell
sudo ufw allow from <adres_IP> to any port <port>
```

Resetowanie ustawień UFW do domyślnych:

```shell
sudo ufw reset
```
