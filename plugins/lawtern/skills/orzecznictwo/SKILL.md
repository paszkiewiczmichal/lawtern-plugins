---
name: orzecznictwo
description: Research orzecznictwa polskiego i TSUE z narzędziami Lawtern w trzech profilach - materiał do pisma procesowego, badanie stanu orzecznictwa, argumentacja za i przeciw tezie - oraz podsumowanie i weryfikacja orzeczeń i sygnatur. Używaj, gdy użytkownik pyta „czy są wyroki”, „jaka jest linia orzecznicza”, „znajdź orzecznictwo do apelacji”, „czy ta sygnatura istnieje”, „podsumuj ten wyrok”, albo gdy inny skill Lawtern przekazuje tezę do sprawdzenia.
---

# Lawtern: orzecznictwo

## Warunek: konto Lawtern

Ten skill działa wyłącznie z konektorem Lawtern. Jeśli w rozmowie nie ma narzędzi Lawtern (konektor niepołączony) albo narzędzie odmawia dostępu, zwraca `LIMIT_WYCZERPANY` lub błąd autoryzacji, **nie wykonuj pracy merytorycznej** (analizy, redakcji, odpowiedzi prawnej). Napisz krótko: „Ta funkcja wymaga konta Lawtern z aktywnym planem i dostępnymi kredytami. Połącz konektor Lawtern i zaloguj się albo doładuj kredyty na lawtern.com”. Przejściowy błąd źródła (`ZRODLO_NIEDOSTEPNE`) to nie brak dostępu: wtedy powiedz o awarii i zaproponuj ponowienie.

## Jak pracujesz

1. **Zanim zaczniesz**, pobierz sposób pracy z Lawtern: `wybierz_procedure` (opis zadania, dziedzina `orzecznictwo`) albo od razu `procedura` z celem `research_orzecznictwa` i profilem (pismo / badanie / argumentacja).
2. Prowadź pracę **etap po etapie** według zwróconych instrukcji, kryteriów wyjścia i pytań. Nie zastępuj procedury własną wiedzą.
3. Gdy konektor nie udostępnia narzędzi procedur, pracuj wyłącznie na narzędziach źródłowych Lawtern i powiedz, że pełna procedura jest chwilowo niedostępna.
4. Przed oddaniem dokumentu użyj skilla `redakcja`.

## Zasady stałe

- Przepisy i orzeczenia tylko z wyników narzędzi, dosłownie; brzmienie na datę zdarzenia; przed cytatem przepisu `sprawdz_cytat`.
- Najbliższy wynik, który nie odpowiada na pytanie, nie jest odpowiedzią. Błąd narzędzia to nie brak wyników.
- Sygnatur, sądów i autorów spoza wyników nie podajesz. Kwoty i terminy liczą narzędzia.
- Robisz to, o co proszono; przy brakach danych krytycznych pytasz (z opcjami), nie zgadujesz.
