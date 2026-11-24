---
name: pytanie-prawne
description: "Odpowiedź na pytanie prawne z prawa polskiego lub unijnego (cywilne, pracy, nieruchomości, spadkowe, rodzinne, karne i wykroczeń, konsumenckie, podatkowe, administracyjne, ochrona danych, dobra osobiste) oparta na przepisach w brzmieniu na datę zdarzenia i orzecznictwie z Lawtern. Use when the user asks a legal question such as „czy mogę”, „czy wolno”, „czy muszę”, „kiedy można / kiedy wolno / kiedy … może” (w sensie warunków, nie daty), „czy przysługuje mi”, „czy odpowiada za”, „czy to jest ważne”, „co grozi za”, „jak złożyć / przeprowadzić / zaskarżyć”, „co zrobić, gdy”, „kto ma rację”, or asks about rights and obligations in a concrete situation, and no contract, pleading or company check is involved."
---

# Lawtern: pytanie prawne

## Kroki

1. **Fakty**: data zdarzenia (od niej zależy brzmienie przepisu), kto jest kim (np. pracownik, konsument, przedsiębiorca), czego użytkownik chce się dowiedzieć. Pytaj tylko o to, co zmienia odpowiedź.
2. **Przepisy**: ustal akt (`szukaj_aktow`, gdy nie znasz aktu albo numeru przepisu; `struktura_aktu`, żeby znaleźć właściwy rozdział) i pobierz brzmienie każdego przepisu, na którym opierasz odpowiedź, `brzmienie_przepisu` z `na_dzien` na datę zdarzenia. Gdy przepis zmieniał się w czasie, `zmiany_aktu`; status aktu `informacja_o_akcie`.
3. **Orzecznictwo**: każdą tezę odpowiedzi sprawdź `szukaj_orzeczen` (z przepisem w `przepis`, cel `badanie`), a orzeczenia, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z ich treści. Gdy kwestia czeka na rozstrzygnięcie SN albo TSUE: `sprawy_w_toku`.
4. **Doktryna i praktyka**: komentarze `szukaj_komentarzy` i `pobierz_komentarz`; decyzje UOKiK, UODO, KNF i interpretacje KIS `szukaj_decyzji`; opracowania Lawtern `szukaj_wiedzy` i `pobierz_wiedze`.
5. **Ścieżka działania**, gdy pytanie dotyczy tego, jak coś zrobić: sąd właściwy `wlasciwy_sad`, opłata `oplata_sadowa`, termin `termin`, przedawnienie `przedawnienie`, rachunek sądu `rachunki_sadu`. Lawtern ma też procedury pracy (`wybierz_procedure`, `procedura`), z których możesz skorzystać jako z listy kontrolnej.
6. **Wynik**: bezpośrednia odpowiedź na pytanie, potem podstawa: przepisy z linkami, orzecznictwo z sygnaturą, datą i linkiem, a przy każdej tezie bez trafnego orzeczenia informacja, że go nie znaleziono. Gdy wynik zależy od faktu, którego nie znasz, pokaż oba warianty.

## Inne skille Lawtern

Przy umowie lub regulaminie do analizy: `umowy`. Przy piśmie procesowym albo decyzji organu: `spory`. Przy sprawdzeniu firmy: `podmioty`. Przy samym obliczeniu terminu lub kwoty: `terminy`.

## Źródła i weryfikacja

- **Podstawa każdej oceny prawnej to przepis i orzecznictwo sprawdzone w Lawtern.** Dotyczy to także oceny, która kończy się wnioskiem, że pisma, zarzutu albo zmiany nie warto składać. (1) Każdy przepis, na którym opierasz ocenę: `brzmienie_przepisu` na datę zdarzenia. (2) Każdą tezę prawną oceny sprawdź w orzecznictwie: `szukaj_orzeczen` (z przepisem w `przepis`), a orzeczenie, które powołujesz, pobierz `pobierz_orzeczenie` i cytuj z jego treści. Gdy nie ma trafnego orzeczenia, napisz to przy tezie.
- Brzmienie przepisu, sygnaturę, treść orzeczenia, dane z rejestru i wynik obliczenia podajesz z wyniku narzędzia Lawtern, z linkiem z pola `link` (Volumina Legum). Adresu nie budujesz sam. Pamięć modelu nie zna dzisiejszego brzmienia przepisów ani bieżącego stanu rejestrów, dlatego tych danych nie podajesz z pamięci.
- Brzmienie przepisu ustalasz na datę zdarzenia (`na_dzien`). Przy `pewnosc_brzmienia` „nieaktualne” cytujesz nowe brzmienie z `tresc_zmiany` nowelizacji, przy „niepewne” zaznaczasz to przy cytacie, przy „uchylony” podajesz datę uchylenia. Dosłowny cytat przepisu bierzesz z wyniku `brzmienie_przepisu`. Przepis przytoczony z innego miejsca (umowa, pismo strony, dokument użytkownika, wcześniejszy tekst) porównujesz przed wstawieniem `sprawdz_cytat`, a rozbieżny zastępujesz brzmieniem z narzędzia.
- Przy kilku przepisach, sygnaturach, podmiotach albo kwotach sprawdzasz każdy osobnym wywołaniem, do końca listy.
- Wynik wyszukiwania, który nie odpowiada na pytanie, nie jest odpowiedzią: piszesz, że nie znaleziono. Brak orzeczenia w bazie nie dowodzi, że ono nie istnieje.
- Błąd narzędzia (np. `ZRODLO_NIEDOSTEPNE`) to nie brak wyników: mówisz o nim i nie wyciągasz wniosków z braku danych. Przy `NIEPRAWIDLOWE_WEJSCIE` poprawiasz argumenty według komunikatu i ponawiasz wywołanie. Gdy narzędzie odmawia dostępu, przekazujesz użytkownikowi sens komunikatu z odpowiedzi, bez własnych dopisków.
- Gdy narzędzi Lawtern nie ma w rozmowie, mówisz o tym i proponujesz podłączenie konektora Lawtern (`https://mcp.lawtern.com/`). Jeśli użytkownik chce pracować bez niego, korzystasz z oficjalnych źródeł publicznych (m.in. isap.sejm.gov.pl, dziennikustaw.gov.pl, orzeczenia.ms.gov.pl, sn.pl, orzeczenia.nsa.gov.pl, eur-lex.europa.eu, curia.europa.eu, wyszukiwarka-krs.ms.gov.pl, biznes.gov.pl) z adresem i datą stanu, a czego nie da się sprawdzić, oznaczasz [niesprawdzone]. Danych z sieci nie przedstawiasz jako sprawdzonych w Lawtern.
- Daty i fakty sprawy bierzesz z materiału użytkownika. Czego w nim nie ma, a zmienia wynik (data zdarzenia, strona, reżim umowy, sąd, kanał doręczenia), o to pytasz, najwyżej 3–4 pytania naraz, z opcjami do wyboru.
