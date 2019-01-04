---
layout: post
title: "[PL] Going with Ionic 3 in My Cookbook app"
categories: MyCookbook
---

## My Cookbook

Co to jest My Cookbook?

My Cookbook jest aplikacją, która jest cyfrową Książką Kucharską oraz Spiżarnią. W Spiżarni możesz śledzić ilość składników, jakie posiadzasz. Na podstawie Twojej Spiżarni aplikacja pokazuje, które potrawy możesz przygotować od razu. Potrawy są oznaczane, kiedy brakuje jakiegoś składnika i aplikacja pokazuje czego brakuje i w jakiej ilości.

MyCookbook został napisany w Ionic v1.

## Cel

Migracja projektu z Ionic v1 do v3.

Podejrzewam, że Ionic v3 jest dosyć stabliny, to do tej wersji chcę aplikację dostosować. Nie będę na razie pchał się do Ionic v4 i tak będzie dla mnie sporo nowości. W szczególności inna wersja Angulara. Już jeden projekt zrobiłem w Angular 2. W momencie jak był jescze dosyć świeży :-).

## Unit tests

Zauważyłem, że nie ma konfiguracji dla testowania kodu testami jednostkowymi.

### Jest

Jest jest test runnerem i frameworkiem wspierającym pisanie testów jednostkowych. Bardzo lubię w jaki sposób używa się Jest'a w konsoli. Myślę, ze w bardzo przejrzysty sposób pokazuje wynik działania testów.

Pogrzebałem w sieci i znalazłem repozytorium https://github.com/datencia/ionic2-jest-example, z którego wziąłem konfigurację dla Jest'a.

### Dependencies

Sposób budowania zależności nie spodobał mi się jaki był przedstawiony w przykładowych testach w repozytorim. Problem polegał na zbyt skomplikowanym przygotowaniem modułów. Zainstalowałem wtyczkę jest-createspyobj i napisałem proste moki za pomocą tej wtyczki.

### Spies Implementation Process

Implementację zrobiłem puszczając testy. Na podstawie logów dostarczyłem kod, który nie powodował błędów. Na tym poziomie nie jest istotne jak faktycznie te moduły są zaimplementowane. Spies mają jedynie udawać, że działają poprawnie.

### Index.ts
By łatwo się importowało Spies przygotowałem zbiorczy plik z exportami.
Tutaj źródło /mocks/index.ts
