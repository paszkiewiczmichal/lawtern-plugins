---
name: spory
description: Praca procesowa w polskim prawie z narzędziami Lawtern - analiza pozwu i pisma procesowego, ocena szans sprawy, odpowiedź na pozew, replika, sprzeciw, przygotowanie pozwu, krytyczne sprawdzenie argumentacji, podsumowanie orzeczenia, chronologia akt (także karnych), pytania do świadków. Używaj, gdy użytkownik załącza lub opisuje pismo procesowe, pozew, wyrok, akta sprawy albo pyta „jakie mamy szanse”, „napisz odpowiedź”, „zrób red team tego pisma”.
---

# Lawtern: spory i pisma procesowe

## Warunek: konto Lawtern

Ten skill działa wyłącznie z narzędziami Lawtern. Gdy ich brakuje albo odmawiają dostępu, **nie wykonuj pracy merytorycznej** (analizy, redakcji, odpowiedzi prawnej). Zamiast tego uprzejmie, w dwóch, trzech zdaniach, powiedz użytkownikowi, co się stało i co ma zrobić. Bez kodów technicznych i bez przeprosin na wyrost. Rodzaj odmowy rozpoznasz po kodzie w błędzie (`kod`); gdy odmowa ma własny komunikat, oprzyj odpowiedź na nim.

| Sytuacja (kod) | Co powiedzieć (sens, własnymi słowami) |
|---|---|
| W rozmowie nie ma narzędzi Lawtern | Do tej pracy potrzebne jest połączenie z Lawtern. Dodaj konektor Lawtern w ustawieniach konektorów i zaloguj się kontem Lawtern; jeśli nie masz konta, załóż je na lawtern.com. |
| Skończyły się kredyty organizacji (`BRAK_KREDYTOW`, `LIMIT_WYCZERPANY`) | Na koncie organizacji skończyły się kredyty Lawtern. Doładuj je na lawtern.com albo poproś administratora organizacji. Gdy będą dostępne, wrócimy do sprawy. |
| Organizacja nie ma planu albo brakuje miejsc (`BRAK_PLANU`) | Twoja organizacja nie ma aktywnego planu Lawtern albo wykorzystała limit miejsc. Wybierz albo zmień plan na lawtern.com, a jeśli plan opłaca organizacja, poproś jej administratora. |
| Plan nie obejmuje tej funkcji (`BRAK_UPRAWNIENIA`) | Plan Twojej organizacji nie obejmuje tej części Lawtern. Skontaktuj się z administratorem organizacji. Nie proponuj zakupu kredytów - nie rozwiążą sprawy. |
| Administrator ograniczył dostęp (`LIMIT_CZLONKA`) | Administrator Twojej organizacji ustawił dla Twojego konta limit albo wyłączył dostęp. Skontaktuj się z nim. |
| Dzienny limit (`LIMIT_DZIENNY`) | Osiągnięto dzienny limit zapytań. Spróbuj ponownie jutro. |
| Konto poza organizacją (`BRAK_CZLONKOSTWA`) | Twoje konto nie należy do organizacji wybranej przy logowaniu. Poproś administratora o zaproszenie albo połącz konektor ponownie i wybierz właściwą organizację. |
| Trzeba połączyć się ponownie (`BRAK_KONTEKSTU`) | Połączenie z Lawtern wymaga odświeżenia. Rozłącz i połącz ponownie konektor Lawtern, a przy logowaniu wybierz swoją organizację. |
| Chwilowa awaria (`ZRODLO_NIEDOSTEPNE`, „chwilowo niedostępne”) | To przejściowa awaria, nie brak dostępu. Zaproponuj ponowienie za chwilę i nie wyciągaj wniosków z braku danych. |
| Źródło odmówiło (`ZRODLO_ZABLOKOWANE`) | Rejestr odmówił odpowiedzi. Nie ponawiaj; wskaż, że dane można sprawdzić bezpośrednio na stronie rejestru. |
| Inna odmowa (`BRAK_DOSTEPU`) | Lawtern odmówił dostępu do tej funkcji. Przekaż komunikat odmowy i zaproponuj kontakt z administratorem organizacji albo z pomocą Lawtern (support@lawtern.com). Nie proponuj zakupu kredytów. |

## Jak pracujesz

1. **Zanim zaczniesz**, pobierz sposób pracy z Lawtern: `wybierz_procedure` (opis zadania, dziedzina `spory`) albo od razu `procedura` z celem odpowiadającym zadaniu (analiza pisma, ocena sporu, pismo odpowiadające, pozew, krytyka argumentacji, chronologia akt, dowód osobowy).
2. Prowadź pracę **etap po etapie** według zwróconych instrukcji, kryteriów wyjścia i pytań. Nie zastępuj procedury własną wiedzą.
3. Gdy konektor nie udostępnia narzędzi procedur, pracuj wyłącznie na narzędziach źródłowych Lawtern i powiedz, że pełna procedura jest chwilowo niedostępna.
4. Przed oddaniem dokumentu użyj skilla `redakcja`.

## Zasady stałe

- Przepisy i orzeczenia tylko z wyników narzędzi, dosłownie; brzmienie na datę zdarzenia; przed cytatem przepisu `sprawdz_cytat`.
- `brzmienie_przepisu`: przy `pewnosc_brzmienia` „nieaktualne” cytuj nowe brzmienie z `tresc_zmiany`; przy „niepewne” zaznacz to przy cytacie.
- Najbliższy wynik, który nie odpowiada na pytanie, nie jest odpowiedzią. Błąd narzędzia to nie brak wyników.
- Sygnatur, sądów i autorów spoza wyników nie podajesz. Kwoty i terminy liczą narzędzia.
- Robisz to, o co proszono; przy brakach danych krytycznych pytasz (z opcjami), nie zgadujesz.
