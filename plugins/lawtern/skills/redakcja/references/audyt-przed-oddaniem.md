# Audyt przed oddaniem

Ostatni przebieg przed oddaniem tekstu użytkownikowi albo przed wysłaniem. Najpierw blok wspólny, potem blok dla gatunku.

## 1. Pętla: szkic, audyt, wersja finalna

1. Przeczytaj polecenie i tekst źródłowy (jeśli redagujesz).
2. Napisz szkic, stosując reguły gatunku na bieżąco.
3. Znajdź w szkicu każde wystąpienie znamion AI (`polskie-zdanie-i-znamiona-ai.md`, sekcja 7).
4. Zadaj sobie pytanie: „Co w tym tekście tak ewidentnie zdradza AI?”. Odpowiedz krótko, wskazując pozostałe sygnały.
5. Popraw do wersji finalnej i przejdź listy poniżej.

Oddajesz wersję finalną; jeśli tekst przeszedł istotną redakcję, dodajesz krótkie punkty „co poprawiono”.

## 2. Blok wspólny (każdy tekst)

- [ ] Brak archaizmów kancelaryjnych.
- [ ] Brak słownictwa AI, wypełniaczy, pustej asekuracji (uzasadniona merytorycznie zostaje).
- [ ] Brak strony biernej z ukrytym sprawcą (poza opisem stanu prawnego).
- [ ] Brak myślnika i półpauzy w funkcji interpunkcyjnej, także ` — `, ` -- ` i dywizu ze spacjami; wyjątki tylko z `typografia-i-format.md`, sekcja 1.
- [ ] Cudzysłów polski „…”.
- [ ] Nagłówki i tematy bez Title Case.
- [ ] Brak emoji i mechanicznych pogrubień.
- [ ] Brak artefaktów rozmowy z asystentem; zakończenie to konkret, nie deklaracja gotowości.
- [ ] Liczby i daty zapisane według konwencji gatunku (`typografia-i-format.md`, sekcja 4).
- [ ] Terminy zdefiniowane użyte identycznie w całym tekście.
- [ ] Przy redakcji: zachowany sens i zakres oryginału.

## 3. Umowa, ugoda, regulamin

- [ ] Każde postanowienie ma wyraźny podmiot; strona czynna, czas teraźniejszy.
- [ ] Każdy obowiązek odpowiada na pytania kto, co, kiedy, jak.
- [ ] Terminy konkretne (liczba dni); brak samego „niezwłocznie”, „odpowiedni”, „powinien”, „tydzień”.
- [ ] Każde pojęcie pisane wielką literą ma definicję; każde pojęcie branżowe jest zdefiniowane.
- [ ] Spójna para nazw stron w całym dokumencie.
- [ ] Kwoty wynagrodzenia i kar cyfrą i słownie; pozostałe liczby według `typografia-i-format.md`, sekcja 4.
- [ ] Hierarchia jednostek zachowana; jeden system wyliczeń na poziomie.
- [ ] Każde odesłanie wewnętrzne prowadzi do istniejącej jednostki; sprawdzone po zakończeniu numeracji.
- [ ] Brak osieroconych załączników.
- [ ] Brak powtórzonej regulacji i odesłań do przepisów bez funkcji prawnej.
- [ ] Brak łaciny w treści klauzul.
- [ ] Szybkie poprawki z `umowy.md`, sekcja 14, przeszły.
- [ ] Pięć pytań legal design (`typografia-i-format.md`, sekcja 7).
- [ ] Projekt własny albo cudzy przeskanowany pod kątem `umowy-frazy-ryzyka.md`.

## 4. Pismo procesowe

- [ ] Struktura i nagłówek według `pisma-procesowe.md`, sekcja 1.
- [ ] Audyt merytoryczny z `pisma-procesowe.md`, sekcja 3, w całości.
- [ ] Wyrenderowany plik obejrzany strona po stronie (obowiązkowo).

## 5. Mail i wiadomość

- [ ] Rozpoznany typ adresata (klient, współpracownik, sąd, urząd, strona przeciwna) i dobrany rejestr.
- [ ] Powitanie i podpis tam, gdzie potrzebne (zwłaszcza pierwszy mail w wątku do klienta albo sądu).
- [ ] Cel maila w pierwszym zdaniu; brak wstępnego bełkotu kancelaryjnego.
- [ ] Jeśli odbiorca był zaniepokojony albo pytał o priorytet, pierwsze zdanie się do tego odnosi.
- [ ] Klient zna skutki czynności, nie tylko fakt.
- [ ] Przy prośbie o zgodę: skutki, zagrożenia, alternatywy (art. 5 pkt 9 KERP).
- [ ] Wiadomo, co odbiorca ma zrobić i do kiedy; następny krok ma termin.
- [ ] Krąg adresatów i osób w kopii właściwy; historia cytowań nie ciągnie zbędnych treści.
- [ ] W piśmie do sądu albo urzędu: sygnatura i podstawa umocowania.

## 6. Opinia, raport, notatka

- [ ] Teza w pierwszym zdaniu albo akapicie.
- [ ] Brak zdań, które nie wnoszą treści.
- [ ] Wnioski konkretne: co, kto, do kiedy.
- [ ] Zastrzeżenie z `opinie-i-notatki.md`, sekcja 4, raz, na końcu analizy.

## 7. Weryfikacja w źródłach

Weryfikacja ma pierwszeństwo przed redakcją: ładny dokument z błędnym cytatem jest gorszy niż brzydki z prawdziwym.

- [ ] Każdy cytowany przepis sprawdzony narzędziem `brzmienie_przepisu`, a cytat narzędziem `sprawdz_cytat`; stan aktu narzędziem `informacja_o_akcie`.
- [ ] Dane stron sprawdzone: `sprawdz_podmiot_krs`; reprezentacja w dacie czynności z przeszłości: `historia_podmiotu_krs`; przedsiębiorca jednoosobowy: `sprawdz_ceidg`.
- [ ] Odsetki policzone narzędziem `odsetki`, terminy narzędziem `termin`, nie w pamięci.

## 8. Bramka przed wersją finalną

Nigdy nie oznaczasz dokumentu jako gotowego do wysłania albo podpisania bez wyraźnego potwierdzenia użytkownika. Przed wersją finalną umowy, klauzuli do wklejenia albo regulaminu zatrzymujesz się i wyświetlasz:

```
⛔ BRAMKA — zanim wygeneruję finalną wersję:
1. Dane stron zweryfikowane (KRS/NIP aktualne)? [sprawdz_podmiot_krs / historia_podmiotu_krs / sprawdz_ceidg lub potwierdzenie ręczne]
2. Cytowane przepisy zweryfikowane? [brzmienie_przepisu, sprawdz_cytat lub potwierdzenie ręczne]
3. Prawnik prowadzący sprawę widział draft?
Potwierdź: „tak, generuj” — lub wskaż co poprawić.
```

Wyjątek: gdy użytkownik powiedział „tryb express” albo „zrób bez pytania”, generujesz, ale dodajesz nagłówek `[DRAFT — DO WERYFIKACJI]`. W trybie LAIK obowiązuje `tekst-dla-laika.md`.

Wiadomości (mail, list) też nie wysyłasz bez pokazania treści do akceptacji.
