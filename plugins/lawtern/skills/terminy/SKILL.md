---
name: terminy
description: Obliczenia prawne przez kalkulatory Lawtern - koniec terminu cywilnego i procesowego, przedawnienie roszczeń, odsetki ustawowe, za opóźnienie i w transakcjach handlowych, opłata sądowa, sąd właściwy, kurs NBP, aktualna data. Używaj, gdy użytkownik pyta „do kiedy mam termin”, „czy roszczenie się przedawniło”, „policz odsetki”, „ile wynosi opłata od pozwu”, „który sąd jest właściwy”, „kurs euro z dnia”.
---

# Lawtern: terminy i kwoty

**Zasada nadrzędna: liczy narzędzie, nie Ty.** Żadnych dat, kwot ani stawek „w głowie”. Gdy narzędzie nie obejmuje przypadku, powiedz to i wskaż, co trzeba policzyć ręcznie.

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

## 1. Które narzędzie

| Pytanie | Narzędzie | Na co uważać |
|---|---|---|
| koniec terminu (dni, tygodnie, miesiące, lata) | `termin` | dla dni data początkowa to dzień zdarzenia (np. doręczenia), który się nie wlicza; przesunięcie na dzień roboczy wg art. 115 KC jest w wyniku; terminy zawite i szczególne reguły ustaw odrębnych wymagają osobnej weryfikacji |
| przedawnienie | `przedawnienie` | wynik orientacyjny: **nie uwzględnia przerwania ani zawieszenia biegu**; wybierz właściwy rodzaj roszczenia |
| odsetki | `odsetki` | wybierz typ: `ustawowe_za_opoznienie` (art. 481 § 2 KC), `ustawowe` (art. 359 § 2 KC) albo `transakcje_handlowe` (B2B); nie dla odsetek umownych; data końcowa nie później niż dziś |
| opłata sądowa | `oplata_sadowa` | |
| sąd właściwy | `wlasciwy_sad` | |
| kurs waluty | `kurs_nbp` | dzień kursu wynika z przepisu, który stosujesz: zapytaj, jeśli nie wiadomo, i nie zakładaj go |
| dzisiejsza data i godzina | `aktualny_czas` | używaj zamiast zakładać datę |

## 2. Dane wejściowe

Brak daty zdarzenia, kwoty albo rodzaju roszczenia to brak krytyczny: zapytaj (z opcjami), nie przyjmuj wartości domyślnej. W relacji B2B zapytaj, czy chodzi o transakcję handlową, zanim policzysz odsetki.

## 3. Wynik

- Wynik narzędzia z podstawą prawną, którą narzędzie zwróciło, i z jego zastrzeżeniami (np. „bez przerwania biegu”, „stopa potwierdzona do …”).
- Rozbicie na podokresy przy odsetkach.
- Gdy wynik trafia do pisma: brzmienie przepisu, na który się powołujesz, sprawdź narzędziem `brzmienie_przepisu`.
- Bez nieproszonych porad procesowych.
