---
name: spory
description: Praca procesowa w polskim prawie z narzędziami Lawtern - analiza pozwu i pisma procesowego, ocena szans sprawy, odpowiedź na pozew, replika, sprzeciw, przygotowanie pozwu, krytyczne sprawdzenie argumentacji, podsumowanie orzeczenia, chronologia akt (także karnych), pytania do świadków. Używaj, gdy użytkownik załącza lub opisuje pismo procesowe, pozew, wyrok, akta sprawy albo pyta „jakie mamy szanse”, „napisz odpowiedź”, „zrób red team tego pisma”.
---

# Lawtern: spory i pisma procesowe

## Warunek: konto Lawtern

Ten skill działa wyłącznie z konektorem Lawtern. Jeśli w rozmowie nie ma narzędzi Lawtern (konektor niepołączony) albo narzędzie odmawia dostępu, zwraca `LIMIT_WYCZERPANY` lub błąd autoryzacji, **nie wykonuj pracy merytorycznej** (analizy, redakcji, odpowiedzi prawnej). Napisz krótko: „Ta funkcja wymaga konta Lawtern z aktywnym planem i dostępnymi kredytami. Połącz konektor Lawtern i zaloguj się albo doładuj kredyty na lawtern.com”. Przejściowy błąd źródła (`ZRODLO_NIEDOSTEPNE`) to nie brak dostępu: wtedy powiedz o awarii i zaproponuj ponowienie.

## Kiedy który tryb

| Polecenie | Tryb |
|---|---|
| „przeanalizuj pozew / pismo”, „sporne i bezsporne fakty” | analiza pisma procesowego |
| „jakie mamy szanse”, „oceń sprawę” | ocena sporu: przesłanka po przesłance, z niepewnością dowodową |
| „napisz odpowiedź / replikę / sprzeciw” | pismo odpowiadające |
| „napisz pozew” | przygotowanie pozwu |
| „zakwestionuj tę argumentację”, „red team” | krytyczne sprawdzenie argumentacji |
| „chronologia z akt” | chronologia akt (także sprawy karne) |
| „pytania do świadka”, „porównaj zeznania” | dowód osobowy |

## 1. Zanim zaczniesz

Ustal (albo zapytaj, z opcjami): **sąd i sygnatura sprawy**, **etap i rodzaj pisma**, **strona**, **daty zdarzeń**, **termin** na czynność (policz go narzędziem `termin`). Gdy brakuje danych krytycznych, zatrzymaj się na pytaniach.

## 2. Procedura Lawtern

Jeśli konektor ma narzędzie `procedura`, wywołaj je z celem odpowiadającym trybowi i prowadź pracę etap po etapie według zwróconych kroków i kryteriów wyjścia.

## 3. Tryb podstawowy (gdy procedury nie ma)

1. **Dane formalne i żądania:** sąd, strony, wartość przedmiotu sporu, żądania, terminy.
2. **Podstawa faktyczna i dowody:** co jest twierdzone, czym udowodnione, co sporne.
3. **Podstawa prawna:** przepisy w brzmieniu na datę zdarzeń (`brzmienie_przepisu` z `na_dzien`), właściwość (`wlasciwy_sad`), opłaty (`oplata_sadowa`), przedawnienie (`przedawnienie`).
4. **Orzecznictwo:** dla każdej tezy, która go wymaga, przekaż sprawę do skilla `orzecznictwo` w profilu **pismo** z pakietem: teza w jednym zdaniu, przepis z aktem, data zdarzenia, sąd sprawy, etap, strona, sygnatury znane z akt (także tezy przeciwnika jako cel kontrargumentów).
5. **Mocne i słabe strony** obu stron, z najpoważniejszym kontrargumentem.
6. **Wynik** (analiza, ocena, projekt pisma) z wyraźnym oddzieleniem: co wynika z materiału sprawy, co z orzeczeń (ze stanem sygnatury), a co jest Twoim wnioskiem.
7. **Kontrola spójności:** czy cytowane orzeczenia i tezy sobie nie przeczą; czy każde twierdzenie ma pokrycie w materiale.
8. **Raport weryfikacji:** co sprawdzono w źródłach, czego nie.

## 4. Zasady

- Sygnatury: tylko z wyników narzędzi albo z akt sprawy, ze stanem sygnatury (skill `orzecznictwo`). Brak w bazie nie dowodzi, że orzeczenie nie istnieje, i nie jest podstawą do zarzutu, że przeciwnik je zmyślił.
- Cytaty z akt: dosłownie, z lokalizacją (strona, karta, akapit).
- Nie zmieniaj po cichu tez, które prawnik już sformułował: pokaż różnicę i zostaw mu decyzję.
- Terminy procesowe liczy `termin`, nie Ty.
- Przed oddaniem pisma zastosuj skill `redakcja`.
- Rób to, o co proszono. Bez nieproszonych porad strategicznych.
