---
name: podmioty
description: Weryfikacja kontrahenta, klienta lub spółki w polskich i unijnych rejestrach przez Lawtern - KRS (aktualny odpis i historia reprezentacji), CEIDG, GUS REGON, Biała Lista VAT i rachunek bankowy, VIES, beneficjenci rzeczywiści (CRBR), upadłość i restrukturyzacja (KRZ), ogłoszenia MSiG. Używaj, gdy użytkownik pyta „sprawdź kontrahenta”, „kto reprezentuje spółkę”, „czy firma jest w upadłości”, „czy rachunek jest na białej liście”, „zrób raport o spółce”, podaje NIP, KRS albo REGON.
---

# Lawtern: podmioty

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

## 1. Ustal, o co chodzi

- **Identyfikator:** NIP, KRS, REGON, PESEL albo nazwa. Z samą nazwą najpierw ustal identyfikator (zapytaj albo wyszukaj), nie zgaduj podmiotu.
- **Data:** stan aktualny czy na dzień czynności (np. podpisania umowy). Reprezentacja w przeszłości wymaga historii, nie aktualnego odpisu.
- **Zakres:** szybkie sprawdzenie (status, reprezentacja, VAT) czy pełny raport.

## 2. Który rejestr

| Pytanie | Narzędzie |
|---|---|
| status, reprezentacja, kapitał spółki dziś | `sprawdz_podmiot_krs` |
| kto reprezentował w dniu czynności | `historia_podmiotu_krs` z `na_dzien` (wynik opiera się na dacie wpisu w KRS, nie zdarzenia: zastrzeż to) |
| jednoosobowa działalność | `sprawdz_ceidg` |
| podmiot po NIP lub REGON | `sprawdz_podmiot_po_nip`, `sprawdz_podmiot_po_regon`, `raport_regon` |
| czy rachunek z faktury jest na Białej Liście | `sprawdz_rachunek_biala_lista` |
| VAT UE | `sprawdz_vat_ue` (bez zapisywania wyników na zapas: odpytuj na bieżąco, numer konsultacji do akt) |
| beneficjenci rzeczywiści | `beneficjenci_rzeczywisci` |
| upadłość, restrukturyzacja | `krz_szukaj_wszedzie` (gdy nie wiesz, jaki to typ podmiotu) albo właściwe `krz_szukaj_*`; obwieszczenia: `krz_obwieszczenia_sprawy` |
| ogłoszenia (głównie sprzed 29.11.2025) | `msig_szukaj` |
| jakie rejestry są dostępne | `lista_rejestrow` |

## 3. Pełny raport (gdy użytkownik o niego prosi)

Jeśli konektor ma narzędzie `procedura`, wywołaj je z celem `raport_podmiotu`. W przeciwnym razie: identyfikacja → KRS lub CEIDG → REGON → Biała Lista → VIES (gdy podmiot jest czynnym podatnikiem VAT UE) → CRBR → KRZ → MSiG, a w wyniku dla każdego rejestru: co zwrócił, z jaką datą stanu, czy wynik jest kompletny.

## 4. Zasady

- Odpowiedź z API rejestru **nie jest dokumentem urzędowym**. Moc dokumentu urzędowego ma samodzielnie pobrany wydruk z wyszukiwarki KRS (art. 4 ust. 4aa ustawy o KRS); zaznacz to, gdy wynik ma trafić do pisma lub umowy.
- KRZ działa bez publicznego API: przejściowa blokada (`KRZ_BLOCKED`) albo `kompletny: false` oznacza, że **brak trafienia nie dowodzi braku wpisu**. Napisz to wprost.
- Błąd narzędzia to nie brak wyników. Nie wyciągaj wniosków z pustki.
- Dane rejestrowe przepisuj dosłownie z wyniku, z datą stanu. Bez nieproszonych ocen wiarygodności kontrahenta.
