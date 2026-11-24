---
name: redakcja
description: "Redakcja językowa, stylistyczna i formalna polskich tekstów prawniczych z regułami redakcji Lawtern: umowy, ugody, regulaminy, klauzule, pisma procesowe, pisma do ZUS, urzędu i innych organów, opinie, notatki, maile do klienta, zespołu, sądu lub urzędu oraz teksty dla osób spoza zawodu. Use when the user asks „popraw styl”, „zredaguj pismo”, „przeredaguj klauzulę”, „wygładź tekst”, „napisz maila do klienta”, „odpisz sądowi”, „odpisz urzędowi”, „przygotuj wersję do wysłania”, „sprawdź przed wysłaniem”, „żeby nie brzmiało jak AI”, „wytłumacz klientowi prostym językiem”. Not for the legal analysis itself (umowy, spory, pytanie-prawne); use it to edit and finalise the text."
---

# Lawtern: redakcja

## Kroki

1. **Rodzaj tekstu**: umowa, pismo procesowe, pismo do organu (ZUS, urząd skarbowy, inny organ), korespondencja (klient, sąd, urząd, zespół), opinia lub notatka, tekst dla osoby spoza zawodu.
2. **Reguły**: pobierz reguły redakcji Lawtern dla rodzaju tekstu, `reguly_redakcji(rodzaj_tekstu)`. Gdy odpowiedź ma `kompletne: false`, pobierz kolejne części (`czesc`), zanim oddasz tekst; typografia i zasady polskiego zdania bywają w dalszych częściach. Sprawdź tekst według reguł i przejdź listę kontroli przed oddaniem, którą zwraca narzędzie.
3. **Treść merytoryczna**: każdy dosłowny cytat przepisu w tekście, który nie pochodzi wprost z wyniku `brzmienie_przepisu`, porównaj przed oddaniem `sprawdz_cytat` (rozbieżny zastąp brzmieniem z narzędzia), sygnatury `sprawdz_sygnatury`, kwoty i terminy kalkulatorami Lawtern (`termin`, `odsetki`, `oplata_sadowa`). Przy przepisie i orzeczeniu podaj link z pola `link`.
4. **Fakty**: daty, nazwiska, kwoty i fakty sprawy bierzesz z materiału użytkownika; czego w nim nie ma, zostawiasz jako pole `[___]` albo pytasz.
5. **Wersja do wysłania lub podpisu**: oddajesz ją po potwierdzeniu użytkownika, że to wersja końcowa.

## Zasady stałe

- Polska typografia: cudzysłów „…”, indeksy górne w numerach artykułów (art. 385¹ KC), spacja nierozdzielająca po skrótach i przed jednostkami.
- Jeden termin na jedno pojęcie w całym tekście; definicje używane konsekwentnie.
- Konkretnie: kto, co, do kiedy, w jakiej formie.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
