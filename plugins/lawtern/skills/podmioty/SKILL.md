---
name: podmioty
description: "Weryfikacja kontrahenta, klienta lub spółki w rejestrach przez Lawtern: KRS (odpis i historia reprezentacji), CEIDG, REGON, Biała Lista VAT i rachunek bankowy, VIES, beneficjenci rzeczywiści (CRBR), upadłość i restrukturyzacja (KRZ), ogłoszenia MSiG. Use when the user gives a NIP, KRS or REGON number or a company name and asks „sprawdź kontrahenta”, „kto reprezentuje spółkę”, „czy firma jest w upadłości”, „czy rachunek jest na białej liście”, „zrób raport o spółce”. Not for assessing a contract with the company (umowy) or its court proceedings (spory)."
---

# Lawtern: podmioty

## Kroki

1. **Identyfikator**: NIP, KRS, REGON albo PESEL. Z samą nazwą najpierw ustal identyfikator (zapytaj albo wyszukaj), nie zgaduj podmiotu.
2. **Dane podstawowe**: NIP `sprawdz_podmiot_po_nip`, KRS `sprawdz_podmiot_krs`, REGON `sprawdz_podmiot_po_regon` albo `raport_regon`, jednoosobowa działalność `sprawdz_ceidg`. Rejestry dostępne w Lawtern: `lista_rejestrow`.
3. **Reprezentacja na dzień czynności** (np. podpisania umowy): `historia_podmiotu_krs`, nie sam aktualny odpis.
4. **VAT i rachunek**: status VAT i rachunek z Białej Listy `sprawdz_rachunek_biala_lista` (NIP i numer rachunku), VAT UE `sprawdz_vat_ue`, numer rachunku przed przelewem `sprawdz_rachunek`.
5. **Beneficjenci rzeczywiści**: `beneficjenci_rzeczywisci`.
6. **Upadłość i restrukturyzacja**: `krz_szukaj_wszedzie` z identyfikatorem; gdy typ podmiotu jest znany, właściwe `krz_szukaj_podmiotu`, `krz_szukaj_przedsiebiorcy` albo `krz_szukaj_osoby`. Sygnatura postępowania KRZ: `krz_szukaj_sygnatury` (nie `sprawdz_sygnatury`). Obwieszczenia: `krz_obwieszczenia_sprawy`.
7. **Ogłoszenia**: `msig_szukaj` i `msig_pobierz_ogloszenie`.
8. **Wynik**: przy każdej danej źródło i dzień sprawdzenia. Rozbieżności między rejestrami wskazujesz wprost.

Procedura pracy Lawtern (`procedura` z celem `raport_podmiotu`) zawiera dobór rejestrów do pełnego raportu i możesz z niej skorzystać jako z listy kontrolnej.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
