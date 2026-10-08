---
name: podmioty
description: Weryfikacja kontrahenta, klienta lub spółki w polskich i unijnych rejestrach przez Lawtern - KRS (aktualny odpis i historia reprezentacji), CEIDG, GUS REGON, Biała Lista VAT i rachunek bankowy, VIES, beneficjenci rzeczywiści (CRBR), upadłość i restrukturyzacja (KRZ), ogłoszenia MSiG. Używaj, gdy użytkownik pyta „sprawdź kontrahenta”, „kto reprezentuje spółkę”, „czy firma jest w upadłości”, „czy rachunek jest na białej liście”, „zrób raport o spółce”, podaje NIP, KRS albo REGON.
---

# Lawtern: podmioty

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
