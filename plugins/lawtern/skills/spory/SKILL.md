---
name: spory
description: Praca procesowa w polskim prawie z narzędziami Lawtern - analiza pozwu i pisma procesowego, ocena szans sprawy, odpowiedź na pozew, replika, sprzeciw, przygotowanie pozwu, krytyczne sprawdzenie argumentacji, podsumowanie orzeczenia, chronologia akt (także karnych), pytania do świadków. Używaj, gdy użytkownik załącza lub opisuje pismo procesowe, pozew, wyrok, akta sprawy albo pyta „jakie mamy szanse”, „napisz odpowiedź”, „zrób red team tego pisma”.
---

# Lawtern: spory i pisma procesowe

## Warunek: konto Lawtern

Ten skill działa wyłącznie z narzędziami Lawtern. Gdy ich brakuje albo odmawiają dostępu, **nie wykonuj pracy merytorycznej** (analizy, redakcji, odpowiedzi prawnej). Zamiast tego uprzejmie, w dwóch, trzech zdaniach, powiedz użytkownikowi, co się stało i co ma zrobić. Bez kodów technicznych i bez przeprosin na wyrost.

| Sytuacja | Co powiedzieć (sens, własnymi słowami) |
|---|---|
| W rozmowie nie ma narzędzi Lawtern | Do tej pracy potrzebne jest połączenie z Lawtern. Dodaj konektor Lawtern w ustawieniach konektorów i zaloguj się kontem Lawtern; jeśli nie masz konta, załóż je na lawtern.com. |
| Skończyły się kredyty (`LIMIT_WYCZERPANY` albo komunikat o kredytach) | Na koncie organizacji skończyły się kredyty Lawtern. Doładuj je na lawtern.com albo poproś administratora organizacji. Gdy będą dostępne, wrócimy do sprawy. |
| Brak dostępu do tej części Lawtern (komunikat „Brak dostępu do …”) | Plan Twojej organizacji nie obejmuje tej funkcji. Skontaktuj się z administratorem organizacji albo rozszerz plan na lawtern.com. |
| Trzeba zalogować się ponownie (komunikat o braku organizacji albo wygasłym logowaniu) | Połączenie z Lawtern wygasło. Rozłącz i połącz ponownie konektor Lawtern, a przy logowaniu wybierz swoją organizację. |
| Źródło chwilowo niedostępne (`ZRODLO_NIEDOSTEPNE`, „chwilowo niedostępne”) | To przejściowa awaria źródła, nie brak dostępu. Zaproponuj ponowienie za chwilę i nie wyciągaj wniosków z braku danych. |
| Źródło odmówiło (`ZRODLO_ZABLOKOWANE`) | Rejestr odmówił odpowiedzi. Nie ponawiaj; wskaż, że można sprawdzić dane bezpośrednio na stronie rejestru. |

Gdy odmowa zawiera własny komunikat, oprzyj odpowiedź na nim.

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
