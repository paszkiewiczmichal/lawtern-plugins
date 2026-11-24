---
name: terminy
description: "Obliczenia prawne kalkulatorami Lawtern: koniec terminu cywilnego i procesowego (także przy e-Doręczeniach, PUE ZUS i portalu informacyjnym), przedawnienie, odsetki ustawowe, za opóźnienie i w transakcjach handlowych, opłata sądowa, sąd właściwy, kurs NBP, PCC, taksa notarialna, aktualna data. Use when the user asks „do kiedy mam termin”, „do kiedy można wnieść apelację / zażalenie / sprzeciw / skargę kasacyjną”, „termin na wniesienie”, „kiedy uprawomocni się wyrok”, „od kiedy liczyć termin przy doręczeniu przez portal informacyjny lub e-Doręczenia”, „czy roszczenie się przedawniło”, „policz odsetki”, „ile wynosi opłata od pozwu”, „który sąd jest właściwy”, „kurs euro z dnia”. Not for deciding whether a claim or right exists, or for „kiedy można / kiedy wolno” in the sense of legal conditions rather than a date (pytanie-prawne) or for drafting the pleading itself (spory)."
---

# Lawtern: terminy i kwoty

## Kroki

1. **Dzisiejsza data**: `aktualny_czas`, gdy wynik zależy od dnia dzisiejszego.
2. **Termin**: `termin` z datą początkową, liczbą i jednostką. Przy doręczeniu podaj `kanal_doreczenia` (papier, e-Doręczenia, PUE ZUS, portal informacyjny) z datą wpłynięcia lub umieszczenia pisma, a `data_odbioru`, jeśli jest w materiale; fikcję doręczenia liczy narzędzie.
3. **Przedawnienie**: `przedawnienie` (nie `termin`).
4. **Odsetki**: `odsetki` z rodzajem odsetek, kwotą i okresem; każdą kwotę i okres osobno.
5. **Opłata i sąd**: `oplata_sadowa`, `wlasciwy_sad`, rachunek sądu `rachunki_sadu`.
6. **Inne**: kurs `kurs_nbp`, podatek od czynności cywilnoprawnych `podatek_pcc`, taksa notarialna `taksa_notarialna`, opłata skarbowa `rachunek_oplaty_skarbowej`, rachunek urzędu skarbowego `rachunki_urzedu_skarbowego`.
7. **Przepis o terminie** (np. art. 369 KPC dla apelacji): sprawdź jego brzmienie `brzmienie_przepisu` na dzień doręczenia i podaj link.
8. **Wynik**: kwota albo data z podstawą prawną i założeniami zwróconymi przez narzędzie. Bez narzędzia pokazujesz podstawę i rachunek krok po kroku, a wynik oznaczasz [niesprawdzone].

Procedura pracy Lawtern (`procedura` z celem `obliczenia`) zawiera dobór kalkulatora do typu obliczenia i możesz z niej skorzystać jako z listy kontrolnej.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
