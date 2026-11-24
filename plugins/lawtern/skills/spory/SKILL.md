---
name: spory
description: "Praca procesowa i przed organami w prawie polskim z Lawtern: analiza pozwu i pisma, ocena szans, odpowiedź na pozew, replika, sprzeciw, apelacja, pozew, chronologia akt (także karnych), pytania do świadków, negocjacje i ugoda, obrona i oskarżenie w sprawie karnej, odwołanie od decyzji ZUS, urzędu skarbowego lub innego organu. Use when the user asks „napisz odpowiedź na pozew”, „sprzeciw od nakazu zapłaty”, „apelacja”, „zażalenie”, „pozew o zapłatę”, „odwołanie od decyzji”, or attaches or describes a pleading, lawsuit, judgment, case file or an authority's decision, or asks „jakie mamy szanse”, „sprawdź argumentację”, „jak odwołać się od decyzji ZUS”, „co odpisać urzędowi”, „przygotuj mnie do negocjacji”, „bronię oskarżonego”. Not for reviewing or drafting a contract (umowy) or for a general legal question without proceedings (pytanie-prawne)."
---

# Lawtern: spory i pisma procesowe

## Kroki

1. **Ustal kontekst**: sąd lub organ, sygnatura, etap, strona użytkownika, data doręczenia i kanał doręczenia (papier, e-Doręczenia, PUE ZUS, portal informacyjny sądów), czego użytkownik oczekuje (ocena, pismo, strategia).
2. **Termin**: `termin` z `kanal_doreczenia` i datą wpłynięcia lub umieszczenia pisma, a z `data_odbioru`, jeśli jest w materiale. Przedawnienie roszczenia: `przedawnienie`. Odsetki do żądania: `odsetki`.
3. **Sąd i koszty**: sąd właściwy miejscowo `wlasciwy_sad` (szczebel ustalasz z przepisów o właściwości rzeczowej), opłata `oplata_sadowa`, rachunek sądu `rachunki_sadu`, przy organie podatkowym `rachunki_urzedu_skarbowego` i `rachunek_oplaty_skarbowej`.
4. **Przepisy**: każdy przepis na datę zdarzenia `brzmienie_przepisu`. Przy ocenie pisma przeciwnika i własnego stanowiska sprawdź też orzecznictwo do każdej tezy (`szukaj_orzeczen`, `pobierz_orzeczenie`), także gdy wniosek brzmi, że pisma nie warto składać.
5. **Orzecznictwo**: tezy `szukaj_orzeczen` (cel `pismo` albo `argumentacja`), treść przed cytatem `pobierz_orzeczenie`. Każdą sygnaturę z pisma przeciwnika i z własnego projektu sprawdź `sprawdz_sygnatury`. Otwarte zagadnienia SN i pytania do TSUE: `sprawy_w_toku`. Praktyka organów: `szukaj_decyzji`.
6. **Strona przeciwna** będąca przedsiębiorcą: `sprawdz_podmiot_krs` albo `sprawdz_ceidg`; upadłość i restrukturyzacja: `krz_szukaj_wszedzie`. Sygnaturę postępowania z KRZ sprawdzasz `krz_szukaj_sygnatury`, nie `sprawdz_sygnatury`.
7. **Cytaty z pisma przeciwnika**: każdy przepis zacytowany w piśmie strony przeciwnej albo w orzeczeniu porównaj `sprawdz_cytat` (z `na_dzien`); rozbieżność wskaż w odpowiedzi.
8. **Pismo**: przed oddaniem pobierz reguły redakcji `reguly_redakcji` (`pismo procesowe` albo `pismo do organu`) i sprawdź według nich tekst; możesz też użyć skilla `redakcja`.
9. **Wynik**: ocena albo pismo z podstawą przy każdym twierdzeniu.

Procedury pracy Lawtern dla sporów (`wybierz_procedure` z dziedziną `spory`, potem `procedura`, np. `analiza-pisma-procesowego`, `ocena-sporu`, `pismo-odpowiadajace`, `przygotowanie-pozwu`, `kwestionowanie-argumentacji`, `dowod-osobowy`, `chronologia-akt-sledztwa`, `negocjacje`, `sprawa-karna`, `postepowanie-przed-organem`) możesz wykorzystać jako listę kontrolną do tych kroków.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
