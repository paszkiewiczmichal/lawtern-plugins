---
name: umowy
description: "Analiza, audyt ryzyk, redakcja i przygotowanie umów, aneksów, ugód i regulaminów w prawie polskim (B2B, IT, IP, SaaS, NDA, body leasing, usługi prawne), z przepisami, klauzulami i danymi stron sprawdzonymi w Lawtern. Use when the user pastes or attaches a contract or asks „sprawdź tę umowę”, „czy mogę to podpisać”, „audyt ryzyk”, „popraw klauzulę”, „napisz umowę / NDA / regulamin”, „przygotuj aneks”, „ugoda”, „jak druga strona to przyjmie”, „sprawdź odesłania”. Not for a legal question without a contract or terms to review (pytanie-prawne) or for court and authority proceedings (spory)."
---

# Lawtern: umowy

## Kroki

1. **Ustal kontekst**: typ umowy, reżim (B2B, konsument, przedsiębiorca na prawach konsumenta, zamówienie publiczne), stronę użytkownika, stan (projekt czy zawarta), datę zawarcia, zakres pracy (szybka ocena, pełna analiza, audyt ryzyk, poprawka fragmentu, nowa umowa, regulamin).
2. **Typ umowy**: `karta_typu_umowy` (kwalifikacja, essentialia, normy bezwzględnie obowiązujące, forma, ryzyka). Kompletność: `lista_kontrolna` (np. `essentialia-mapowanie`, `checklist-15`, przy powierzeniu danych `checklist-dpa-art28`).
3. **Strony umowy**: każdą stronę sprawdź w rejestrze, `sprawdz_podmiot_krs` albo `sprawdz_ceidg` (z samym NIP: `sprawdz_podmiot_po_nip`). Reprezentację na dzień podpisania ustal `historia_podmiotu_krs`. Rachunek do płatności: `sprawdz_rachunek_biala_lista`.
4. **Postanowienia**: dla każdej istotnej klauzuli `porownaj_klauzule` (reguły budowy, red flags, wzorcowe brzmienie), brzmienie zastępcze z `szukaj_klauzul` i `pobierz_klauzule`, reguły i doktryna z `szukaj_wiedzy` i `pobierz_wiedze`. Dla każdego istotnego ryzyka (np. ważność, abuzywność, miarkowanie kary) sprawdź orzecznictwo `szukaj_orzeczen` z przepisem i pobierz powoływane orzeczenia `pobierz_orzeczenie`.
5. **Przepisy**: zanim ocenisz postanowienie, pobierz brzmienie przepisów, które je regulują (z kodeksu cywilnego, ustaw szczególnych i przepisów unijnych, które dotyczą danego rodzaju postanowienia). Każdy przepis powołany w umowie albo w Twojej ocenie sprawdź `brzmienie_przepisu` na datę zawarcia umowy. Praktyka organów (UOKiK przy klauzulach konsumenckich, UODO przy danych): `szukaj_decyzji`.
6. **Regulamin i wzorzec umowny** (sklep, serwis, konsument): każdą klauzulę oceń `porownaj_klauzule` z `rezim` `konsument` albo `przedsiebiorca_na_prawach_konsumenta`, wzorcowe brzmienie z `szukaj_klauzul`; abuzywność sprawdź w orzecznictwie `szukaj_orzeczen` z przepisem art. 385¹ KC i w decyzjach UOKiK `szukaj_decyzji` (organ `UOKiK`).
7. **Odesłania wewnętrzne** (paragrafy, załączniki, definicje): sprawdź, czy cel istnieje i pasuje.
8. **Kwoty i terminy** z umowy licz narzędziami: `odsetki`, `termin`, `przedawnienie`, przy PCC `podatek_pcc`, przy akcie notarialnym `taksa_notarialna`.
9. **Cytat przepisu**: przepis zacytowany w umowie porównaj `sprawdz_cytat` (z `na_dzien` na datę zawarcia); rozbieżność wskaż jako ryzyko.
10. **Wynik**: ryzyka z oceną, podstawą i propozycją brzmienia. Przed oddaniem tekstu umowy użyj skilla `redakcja`.

Procedury pracy Lawtern dla umów (`wybierz_procedure` z dziedziną `umowy`, potem `procedura`, np. `triage-szybki`, `pelna-analiza`, `audyt-ryzyk`, `generator-umow`, `generator-regulaminu`, `ocena-2-strony`, `weryfikacja-spojnosci-odeslan`) możesz wykorzystać jako listę kontrolną do tych kroków.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
