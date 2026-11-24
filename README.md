# Lawtern dla Claude

Lawtern to warstwa wiedzy i umiejętności dla twojego narzędzia AI. Plugin dodaje do Claude konektor Lawtern i osiem gotowych umiejętności pracy z polskim prawem. Asystent dostaje przepisy w brzmieniu na dany dzień, orzecznictwo, rejestry firm, kalkulatory i 25 procedur pracy prawnika, a przy każdym przepisie i orzeczeniu daje link do pełnego tekstu.

Więcej: [lawtern.com](https://lawtern.com/) · [Konektor Lawtern](https://lawtern.com/konektor/) · [Dokumentacja](https://docs.lawtern.com/)

## Co dostajesz

| Umiejętność | Co robi |
|---|---|
| `pytanie-prawne` | Odpowiedź na pytanie prawne z przepisem w brzmieniu na dzień zdarzenia i orzecznictwem. |
| `asystent` | Odpowiedź z podstawą prawną. Asystent dopyta o brakujące fakty i odpowie z przepisem w brzmieniu na właściwy dzień. |
| `orzecznictwo` | Wyroki w podobnych sprawach i argumenty, które przekonały sąd, gotowe do pisma. |
| `podmioty` | Sprawdzony kontrahent: KRS, CEIDG, biała lista VAT, beneficjenci rzeczywiści i rejestr zadłużonych w jednej odpowiedzi. |
| `umowy` | Ryzyka w umowie, lepsze brzmienie klauzul albo cały projekt umowy. |
| `spory` | Pozew, odpowiedź na pozew albo sprzeciw z chronologią zdarzeń, pytaniami do świadków i propozycją ugody. |
| `terminy` | Terminy z dniami wolnymi, przedawnienie, odsetki, opłata sądowa i sąd właściwy. |
| `redakcja` | Pismo, umowa albo wiadomość w prostym języku, ze spójnymi pojęciami i sprawdzonymi cytatami. |

Przykłady poleceń:

- „Jak brzmiał art. 484 § 2 k.c. 1 marca 2024 r.? Podaj link do źródła.”
- „Sprawdź kontrahenta przed podpisaniem umowy: [NIP]. Kto reprezentuje spółkę, czy rachunek z faktury jest na białej liście VAT i czy jest wpis w Krajowym Rejestrze Zadłużonych?”
- „Wyrok doręczono mi przez portal informacyjny 3 listopada 2026 r., odebrałem go 10 listopada. Do kiedy mam termin na apelację?”

Umiejętności uruchamiasz poleceniem, na przykład `/lawtern:umowy Przygotuj rewizję tej umowy. Zwróć szczególną uwagę na kary umowne.`, albo po prostu piszesz, czego potrzebujesz.

## Z jakich narzędzi Lawtern korzystają umiejętności

Konektor Lawtern daje Claude narzędzia z pięciu grup. Umiejętności wskazują, którego narzędzia użyć na którym kroku pracy.

- **Przepisy**: `brzmienie_przepisu` (brzmienie na dany dzień), `sprawdz_cytat`, `szukaj_aktow`, `struktura_aktu`, `zmiany_aktu`, `informacja_o_akcie`.
- **Orzecznictwo i praktyka organów**: `szukaj_orzeczen`, `pobierz_orzeczenie`, `sprawdz_sygnatury`, `sprawdz_orzeczenie_tsue`, `sprawy_w_toku`, `szukaj_decyzji`, `pobierz_decyzje`, `szukaj_komentarzy`, `pobierz_komentarz`.
- **Rejestry**: `sprawdz_podmiot_po_nip`, `sprawdz_podmiot_krs`, `historia_podmiotu_krs`, `sprawdz_ceidg`, `raport_regon`, `sprawdz_rachunek_biala_lista`, `sprawdz_vat_ue`, `beneficjenci_rzeczywisci`, `krz_szukaj_wszedzie`, `krz_szukaj_sygnatury`, `msig_szukaj`.
- **Kalkulatory**: `termin`, `przedawnienie`, `odsetki`, `oplata_sadowa`, `wlasciwy_sad`, `kurs_nbp`, `podatek_pcc`, `taksa_notarialna`.
- **Wiedza Lawtern**: `karta_typu_umowy`, `lista_kontrolna`, `szukaj_klauzul`, `porownaj_klauzule`, `szukaj_wiedzy`, `reguly_redakcji`, `wybierz_procedure`, `procedura`.

Wszystkie narzędzia tylko odczytują dane. Działają po zalogowaniu kontem Lawtern.

## Czego potrzebujesz

- płatnego planu Claude (Pro, Max, Team albo Enterprise);
- konta Lawtern. Załóż je na [account.lawtern.com](https://account.lawtern.com/), a na start dostaniesz 150 kredytów. Plany i paczki opisuje [cennik](https://lawtern.com/cennik/).

## Instalacja

### claude.ai, Claude Desktop i Cowork

1. Otwórz Customize, potem Plugins, Add i Add marketplace.
2. Wybierz Add from a repository i wpisz `paszkiewiczmichal/lawtern-plugins`.
3. Przy pluginie Lawtern kliknij Add.
4. W zakładce Connectors pluginu kliknij Connect, zaloguj się kontem Lawtern i zatwierdź dostęp.
5. Zacznij nową rozmowę i zapytaj, na przykład „Jak brzmi art. 455 k.c.?”.

### Claude Code

```
/plugin marketplace add paszkiewiczmichal/lawtern-plugins
/plugin install lawtern@lawtern-plugins
```

Przy pierwszym użyciu narzędzia Lawtern zaloguj się przez `/mcp` i wybierz `lawtern`.

### Cała organizacja (Team i Enterprise)

Owner dodaje marketplace w Organization settings, w sekcji Plugins, i udostępnia plugin wszystkim członkom. Szczegóły w [dokumentacji](https://docs.lawtern.com/).

### Bez pluginu

Sam konektor dodasz w Claude i ChatGPT adresem `https://mcp.lawtern.com/`. Instrukcja: [lawtern.com/konektor](https://lawtern.com/konektor/#reczny).

## Aktualizacje

Plugin aktualizuje się razem z marketplace. Nowe procedury i źródła działają od razu, bo są po stronie serwera Lawtern.

## Pomoc

[contact@lawtern.com](mailto:contact@lawtern.com) · [Regulamin](https://docs.lawtern.com/#legal-regulamin) · [Polityka prywatności](https://docs.lawtern.com/#legal-polityka-prywatnosci)

Lawtern tworzy Kancelaria Radcy Prawnego Michał Paszkiewicz, Gdańsk.

## Licencja

Apache License 2.0 (`LICENSE`).
