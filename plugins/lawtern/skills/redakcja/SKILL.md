---
name: redakcja
description: Redakcja językowa, stylistyczna i formalna polskich tekstów prawniczych i kancelaryjnych (umowy, ugody, regulaminy, klauzule, pisma procesowe, opinie, notatki, maile i wiadomości do klienta, zespołu, sądu lub urzędu) oraz tekstów prawnych dla osób spoza zawodu. Pilnuje rejestru prawniczego, precyzji klauzul i polskiej typografii, usuwa znamiona tekstu generowanego przez AI, a przed oddaniem przeprowadza audyt i bramkę wersji finalnej. Używaj, gdy użytkownik prosi „popraw styl”, „zredaguj pismo”, „przeredaguj klauzulę”, „wygładź tekst”, „napisz maila do klienta”, „odpisz sądowi” albo „odpisz urzędowi”, „przygotuj wersję do wysłania”, „sprawdź przed wysłaniem”, „żeby nie brzmiało jak AI”, „wytłumacz klientowi prostym językiem”, a także przed oddaniem każdego dokumentu przygotowanego w skillach umowy i spory.
---

# Lawtern: redakcja

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

## Jak pracujesz

1. Ustal rodzaj tekstu: umowa / pismo procesowe / korespondencja (klient, sąd, urząd, zespół) / opinia lub notatka / tekst dla laika.
2. **Zanim zaczniesz redagować**, pobierz reguły: `reguly_redakcji(rodzaj_tekstu)`. Stosuj je w podanej kolejności i przeprowadź audyt przed oddaniem, który narzędzie zwraca.
3. Dane, cytaty, kwoty i terminy w tekście pochodzą z narzędzi Lawtern, nie z pamięci.
- `brzmienie_przepisu`: przy `pewnosc_brzmienia` „nieaktualne” cytuj nowe brzmienie z `tresc_zmiany`; przy „niepewne” zaznacz to przy cytacie.
4. Wersję do wysłania lub podpisu oddajesz dopiero po jawnym potwierdzeniu użytkownika.
