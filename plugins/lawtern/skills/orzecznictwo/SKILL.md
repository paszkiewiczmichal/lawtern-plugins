---
name: orzecznictwo
description: Research orzecznictwa polskiego i TSUE z narzędziami Lawtern w trzech profilach - materiał do pisma procesowego, badanie stanu orzecznictwa, argumentacja za i przeciw tezie - oraz podsumowanie i weryfikacja orzeczeń i sygnatur. Używaj, gdy użytkownik pyta „czy są wyroki”, „jaka jest linia orzecznicza”, „znajdź orzecznictwo do apelacji”, „czy ta sygnatura istnieje”, „podsumuj ten wyrok”, albo gdy inny skill Lawtern przekazuje tezę do sprawdzenia.
---

# Lawtern: orzecznictwo

Pracujesz według metodologii kancelarii i zasad serwera Lawtern. Ten skill ich nie zmienia: pokazuje, jak z nich korzystać krok po kroku.

## 1. Profil celu (parametr `cel` w `szukaj_orzeczen`)

| Profil | Kiedy | Czego potrzebujesz na wejściu | Co musi być w wyniku |
|---|---|---|---|
| **pismo** | materiał do konkretnego pisma | sąd sprawy (`sad_sprawy`), teza, data zdarzeń, etap, strona | orzeczenia najwyższej mocy i z sądu sprawy, fragmenty do cytowania z lokalizacją, najpoważniejszy kontrargument |
| **badanie** | poznanie stanu orzecznictwa | pytanie, data stanu prawnego | obie linie (jeśli są), rozbieżności, sprawy zawisłe (`sprawy_w_toku`), stan prawny na datę, metoda i kryteria doboru |
| **argumentacja** | budowa i sprawdzenie stanowiska | teza (`teza` uruchamia kontrresearch), strona | racje za i przeciw osobno, z trybem: ocena sądu / obiter / referowane |

Gdy profil nie wynika z polecenia, zapytaj jednym pytaniem z trzema opcjami. W profilu **pismo** brak sądu sprawy albo daty zdarzeń to brak krytyczny: zapytaj przed wyszukiwaniem.

Pakiet od innych skilli (`umowy`, `spory`): cel, teza w jednym zdaniu, przepis z aktem (nie sam skrót), data zdarzenia, sąd sprawy, etap, strona, sygnatury znane z akt. Wynik oddajesz bez spłaszczania: moc formalna, kto mówi, aktualność, kontrargumenty, pokrycie korpusu, stany sygnatur.

## 2. Przebieg

1. **Zapytania:** co najmniej trzy, równolegle, w trzech warstwach: reguła (co przepis nakazuje lub dopuszcza), granica negatywna (kiedy reguła nie działa), obowiązek symetryczny (co z drugiej strony). Przepis podawaj w parametrze `przepis` z aktem.
2. **Podnieś autorytety do lektury.** Z sekcji `gwarantowane_miejsca` i `autorytety_cytowane` pobierz (`pobierz_orzeczenie`) co najmniej uchwały z mocą zasady prawnej lub składu 7 sędziów i wyroki TSUE, jeśli dotyczą pytania, **zanim cokolwiek napiszesz**. To jest najczęstszy błąd: wzorcowe orzeczenia są w wynikach narzędzia, ale nie trafiają do odpowiedzi.
3. **TSUE:** czytaj ocenę Trybunału, nie stanowisko sądu odsyłającego ani rządów. Pobierz sentencję (`pobierz_orzeczenie` z `koniec=true`) i część „W przedmiocie pytań prejudycjalnych”.
4. **Lektura przed cytatem:** cytujesz tylko to, co przeczytałeś w treści orzeczenia. Sprawdź, czyje to słowa: sądu orzekającego, strony, sądu niższej instancji, innego orzeczenia. Nie pisz „sąd uznał”, dopóki treść tego nie potwierdza.
5. **Sygnatury spoza wyników** (z pisma przeciwnika, z pamięci, od użytkownika): najpierw `sprawdz_sygnatury`, potem treść przez `pobierz_orzeczenie`. Istnienie sygnatury nie potwierdza tezy.
6. **Kontrola spójności:** gdy wynik cytuje więcej niż jedno orzeczenie, sprawdź, czy nie mówią rzeczy przeciwnych (references/dyscyplina-orzecznictwa.md § 5).

## 3. Wynik

- Przy każdym orzeczeniu: sąd, data, sygnatura z wyników, **moc formalna** (z narzędzia, słowami: np. „uchwała 7 sędziów SN, bez mocy zasady prawnej”; nie używaj słowa „precedens”), kto mówi, cytat z lokalizacją, **stan sygnatury** (references/dyscyplina-orzecznictwa.md § 1).
- Teza redakcyjna to nie uzasadnienie: oznaczaj, skąd pochodzi zdanie.
- Aktualność przepisu (brzmienie na datę) i aktualność argumentu jako osobne informacje.
- **Kontrargumenty** jako stała sekcja w profilach pismo i argumentacja. Gdy ich nie znaleziono, napisz, przy jakich zapytaniach i jakie są ograniczenia korpusu, a nie „brak kontrargumentów”.
- **Metoda:** zapytania, filtry, czego korpus nie obejmuje (m.in. sądy administracyjne; doktryna tylko za cytatem w orzeczeniu, chyba że masz dostęp do komentarzy).
- Cytat z orzeczenia nie dostaje etykiety „zweryfikowany”: automatyczne sprawdzenie cytatu działa dziś tylko dla przepisów (`sprawdz_cytat`).

## 4. Zasady

Przepisy i orzeczenia tylko z wyników narzędzi, dosłownie. Najbliższy wynik, który nie odpowiada na pytanie, nie jest odpowiedzią. Błąd narzędzia to nie brak wyników. Rób to, o co proszono, bez nieproszonych porad. Pełna dyscyplina: `references/dyscyplina-orzecznictwa.md`.
