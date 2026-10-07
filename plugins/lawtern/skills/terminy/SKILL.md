---
name: terminy
description: Obliczenia prawne przez kalkulatory Lawtern - koniec terminu cywilnego i procesowego, przedawnienie roszczeń, odsetki ustawowe, za opóźnienie i w transakcjach handlowych, opłata sądowa, sąd właściwy, kurs NBP, aktualna data. Używaj, gdy użytkownik pyta „do kiedy mam termin”, „czy roszczenie się przedawniło”, „policz odsetki”, „ile wynosi opłata od pozwu”, „który sąd jest właściwy”, „kurs euro z dnia”.
---

# Lawtern: terminy i kwoty

## Warunek: konto Lawtern

Ten skill działa wyłącznie z konektorem Lawtern. Jeśli w rozmowie nie ma narzędzi Lawtern (konektor niepołączony) albo narzędzie odmawia dostępu, zwraca `LIMIT_WYCZERPANY` lub błąd autoryzacji, **nie wykonuj pracy merytorycznej** (analizy, redakcji, odpowiedzi prawnej). Napisz krótko: „Ta funkcja wymaga konta Lawtern z aktywnym planem i dostępnymi kredytami. Połącz konektor Lawtern i zaloguj się albo doładuj kredyty na lawtern.com”. Przejściowy błąd źródła (`ZRODLO_NIEDOSTEPNE`) to nie brak dostępu: wtedy powiedz o awarii i zaproponuj ponowienie.

## Jak pracujesz

1. **Zanim zaczniesz**, pobierz sposób pracy z Lawtern: `wybierz_procedure` (opis zadania, dziedzina `terminy`) albo od razu `procedura` z celem `obliczenia`.
2. Prowadź pracę **etap po etapie** według zwróconych instrukcji, kryteriów wyjścia i pytań. Nie zastępuj procedury własną wiedzą.
3. Gdy konektor nie udostępnia narzędzi procedur, pracuj wyłącznie na narzędziach źródłowych Lawtern i powiedz, że pełna procedura jest chwilowo niedostępna.
4. Przed oddaniem dokumentu użyj skilla `redakcja`.

## Zasady stałe

- Przepisy i orzeczenia tylko z wyników narzędzi, dosłownie; brzmienie na datę zdarzenia; przed cytatem przepisu `sprawdz_cytat`.
- `brzmienie_przepisu`: przy `pewnosc_brzmienia` „nieaktualne” cytuj nowe brzmienie z `tresc_zmiany`; przy „niepewne” zaznacz to przy cytacie.
- Najbliższy wynik, który nie odpowiada na pytanie, nie jest odpowiedzią. Błąd narzędzia to nie brak wyników.
- Sygnatur, sądów i autorów spoza wyników nie podajesz. Kwoty i terminy liczą narzędzia.
- Robisz to, o co proszono; przy brakach danych krytycznych pytasz (z opcjami), nie zgadujesz.
