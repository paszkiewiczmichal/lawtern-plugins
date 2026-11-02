# Lawtern dla Claude

Lawtern to warstwa wiedzy i umiejętności dla twojego narzędzia AI. Plugin dodaje do Claude konektor Lawtern i siedem gotowych umiejętności pracy z polskim prawem. Asystent dostaje przepisy w brzmieniu na dany dzień, orzecznictwo, rejestry firm, kalkulatory i 24 procedury pracy prawnika, a przy każdym przepisie i orzeczeniu daje link do pełnego tekstu.

Więcej: [lawtern.com](https://lawtern.com/) · [Konektor Lawtern](https://lawtern.com/konektor/) · [Dokumentacja](https://docs.lawtern.com/)

## Co dostajesz

| Umiejętność | Co robi |
|---|---|
| `asystent` | Odpowiedź z podstawą prawną. Asystent dopyta o brakujące fakty i odpowie z przepisem w brzmieniu na właściwy dzień. |
| `orzecznictwo` | Wyroki w podobnych sprawach i argumenty, które przekonały sąd, gotowe do pisma. |
| `podmioty` | Sprawdzony kontrahent: KRS, CEIDG, biała lista VAT, beneficjenci rzeczywiści i rejestr zadłużonych w jednej odpowiedzi. |
| `umowy` | Ryzyka w umowie, lepsze brzmienie klauzul albo cały projekt umowy. |
| `spory` | Pozew, odpowiedź na pozew albo sprzeciw z chronologią zdarzeń, pytaniami do świadków i propozycją ugody. |
| `terminy` | Terminy z dniami wolnymi, przedawnienie, odsetki, opłata sądowa i sąd właściwy. |
| `redakcja` | Pismo, umowa albo wiadomość w prostym języku, ze spójnymi pojęciami i sprawdzonymi cytatami. |

Umiejętności uruchamiasz poleceniem, na przykład `/lawtern:umowy Przygotuj rewizję tej umowy. Zwróć szczególną uwagę na kary umowne.`, albo po prostu piszesz, czego potrzebujesz.

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
