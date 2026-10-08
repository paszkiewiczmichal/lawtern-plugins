---
name: umowy
description: Analiza, audyt ryzyk, redakcja i generowanie umów oraz regulaminów w polskim prawie (B2B, IT, IP, SaaS, NDA, body leasing, usługi prawne, ugody), z weryfikacją przepisów i stron w źródłach Lawtern. Używaj, gdy użytkownik wkleja lub załącza umowę, prosi o „sprawdź tę umowę”, „czy mogę to podpisać”, „audyt ryzyk”, „popraw klauzulę”, „napisz umowę / NDA / regulamin”, „jak druga strona to przyjmie”, „sprawdź odesłania”.
---

# Lawtern: umowy

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
| „szybko sprawdź”, „czy to OK do podpisania” | szybka ocena: zielone / żółte / czerwone, najważniejsze ryzyka |
| „przeanalizuj”, „sprawdź umowę” | pełna analiza (etapami) |
| „jakie są ryzyka”, „co tu jest niebezpieczne” | audyt ryzyk z poziomami |
| „popraw § X”, „zmień tę klauzulę” | poprawka fragmentu |
| „napisz umowę / NDA / regulamin” | generowanie (wywiad → szkielet → treść) |
| „jak druga strona to przyjmie”, „co przeoczyliśmy” | ocena oczami drugiej strony |
| „sprawdź odesłania”, długa umowa | kontrola spójności odesłań (osobne przejście: najpierw spis, potem sprawdzenie każdego odesłania) |

## 1. Zanim zaczniesz

Ustal (albo zapytaj, z opcjami): **czyją stronę reprezentujesz**, **reżim** (B2B / konsument / osoba fizyczna-przedsiębiorca bez zawodowego charakteru umowy, art. 385⁵ KC), **typ i stan umowy** (projekt / zawarta, data zawarcia), **cel** (ocena, negocjacje, podpis). Przy brakach krytycznych zatrzymaj się na pytaniach.

## 2. Procedura Lawtern

Jeśli konektor ma narzędzie `procedura`, wywołaj je z celem odpowiadającym trybowi (np. `analiza_umowy`) i prowadź pracę etap po etapie według zwróconych kroków i kryteriów wyjścia. Reguły budowy umowy danego typu (kwalifikacja, essentialia, normy bezwzględnie obowiązujące, ryzyka) bierz z `karta_typu_umowy`, a przykłady klauzul, listy kontrolne i wiedzę z `szukaj_klauzul`, `porownaj_klauzule`, `lista_kontrolna`, `szukaj_wiedzy`, jeśli są dostępne. Umowę piszesz według reguł, nie przez kopiowanie gotowego wzoru.

## 3. Tryb podstawowy (gdy procedury nie ma)

Pracuj etapami i **zatrzymuj się po każdym etapie** na korekty użytkownika (chyba że poprosi o całość naraz; wtedy oznacz miejsca, w których normalnie byś się zatrzymał):
1. **Materiał i założenia:** co analizujesz, czyją stronę, jaki reżim, jaki cel.
2. **Kwalifikacja:** jaki to typ umowy w świetle przepisów i jakie przepisy bezwzględnie obowiązujące go dotyczą. Sprawdź je narzędziem `brzmienie_przepisu` (z `na_dzien`, gdy umowa jest zawarta).
3. **Ekstrakcja:** strony, przedmiot, wynagrodzenie, terminy, odpowiedzialność, rozwiązanie, elementy szczególne (dane osobowe, prawa autorskie, podwykonawcy).
4. **Braki krytyczne i istotne:** krytyczne blokują wersję do podpisu, istotne zwiększają ryzyko sporu.
5. **Ryzyka z podstawą:** każde ryzyko z cytatem z dokumentu (§, ust.), skutkiem, wagą i rekomendacją. Podstawę prawną ryzyka sprawdź w źródle. Gdy ryzyko zależy od wykładni sądów, przekaż je do skilla `orzecznictwo` z pakietem: cel, teza w jednym zdaniu, przepis z aktem, data zdarzenia, strona.
6. **Propozycje brzmień** dopasowane do strony i reżimu, w układzie „było / proponowane / uzasadnienie”.
7. **Kontrola spójności:** czy rekomendacje sobie nie przeczą i czy nie naruszają przepisów bezwzględnie obowiązujących (np. odpowiedzialność za szkodę umyślną, art. 473 § 2 KC; ochrona z art. 385¹ i nast. KC).
8. **Raport weryfikacji:** co sprawdzono w źródłach, czego nie.

## 4. Zasady

- Dane stron weryfikuj w rejestrach (skill `podmioty`), reprezentację na dzień czynności przez `historia_podmiotu_krs`.
- Kwoty i terminy liczą narzędzia (`odsetki`, `termin`, `przedawnienie`).
- Przepisy tylko z wyników narzędzi, dosłownie, z `sprawdz_cytat` przed wstawieniem. Sygnatur nie podajesz z pamięci.
- **Wersja do podpisu** tylko po jawnym potwierdzeniu użytkownika: dane stron sprawdzone, cytaty sprawdzone, prawnik widział szkic. Bez potwierdzenia albo przy brakach: szkic z polami `[___]`.
- Przed oddaniem dokumentu zastosuj skill `redakcja`.
- Rób to, o co proszono. Bez nieproszonych porad.
