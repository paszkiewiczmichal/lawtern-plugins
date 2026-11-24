---
name: orzecznictwo
description: "Research orzecznictwa polskiego, TSUE i ETPCz z Lawtern: materiał do pisma, stan orzecznictwa, argumenty za i przeciw tezie, podsumowanie wyroku, sprawdzenie sygnatur. Use when the user asks „czy są wyroki”, „jaka jest linia orzecznicza”, „znajdź orzecznictwo do apelacji”, „czy ta sygnatura istnieje”, „podsumuj ten wyrok”, or needs case law to support or test a legal thesis. For a complete answer to a legal question, combining statutes and case law, use pytanie-prawne; for a pleading, spory."
---

# Lawtern: orzecznictwo

## Kroki

1. **Ustal cel**: materiał do pisma (`pismo`), stan orzecznictwa (`badanie`) albo argumenty za i przeciw tezie (`argumentacja`); sąd sprawy i przepis, którego dotyczy pytanie.
2. **Szukaj**: `szukaj_orzeczen` z celem, przepisem (`przepis`) i sądem sprawy (`sad_sprawy`). Przy tezie podaj `teza`, żeby dostać kontrautorytety do sprawdzenia. Kolejne strony przez `offset`.
3. **Czytaj przed cytatem**: każde orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Uchwały SN i wyroki TSUE z sekcji `gwarantowane_miejsca` pobierz, jeśli dotyczą pytania. Odróżniaj ocenę sądu od stanowiska strony i od cytatu innego orzeczenia.
4. **Sygnatury**: każdą sygnaturę podaną przez użytkownika albo z pisma sprawdź `sprawdz_sygnatury`; orzeczenia TSUE `sprawdz_orzeczenie_tsue`. Sygnatury postępowań z KRZ sprawdza `krz_szukaj_sygnatury`.
5. **Kwestie otwarte**: `sprawy_w_toku` (zagadnienia przed SN, pytania prejudycjalne do TSUE).
6. **Praktyka organów** (UOKiK, UODO, KNF, interpretacje KIS): `szukaj_decyzji` i `pobierz_decyzje`; to nie są orzeczenia sądów.
7. **Wynik**: dla każdego orzeczenia sąd, data, sygnatura, link, teza z treści i jej znaczenie dla sprawy. Opinia rzecznika generalnego TSUE nie wiąże: przedstawiasz ją jako stanowisko rzecznika.

Procedury pracy Lawtern (`procedura` z celem `research_orzecznictwa` albo `podsumowanie-orzeczenia`) możesz wykorzystać jako listę kontrolną do tych kroków.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
