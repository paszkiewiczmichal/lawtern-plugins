---
name: redakcja
description: Redakcja językowa, stylistyczna i formalna polskich tekstów prawniczych i kancelaryjnych (umowy, ugody, regulaminy, klauzule, pisma procesowe, opinie, notatki, maile i wiadomości do klienta, zespołu, sądu lub urzędu) oraz tekstów prawnych dla osób spoza zawodu. Pilnuje rejestru prawniczego, precyzji klauzul i polskiej typografii, usuwa znamiona tekstu generowanego przez AI, a przed oddaniem przeprowadza audyt i bramkę wersji finalnej. Używaj, gdy użytkownik prosi „popraw styl”, „zredaguj pismo”, „przeredaguj klauzulę”, „wygładź tekst”, „napisz maila do klienta”, „odpisz sądowi” albo „odpisz urzędowi”, „przygotuj wersję do wysłania”, „sprawdź przed wysłaniem”, „żeby nie brzmiało jak AI”, „wytłumacz klientowi prostym językiem”, a także przed oddaniem każdego dokumentu przygotowanego w skillach umowy i spory.
---

# Lawtern: redakcja

Ten skill kontroluje warstwę językową, stylistyczną i formalną tekstu. Nie analizuje ryzyk, nie ocenia szans sprawy i nie cytuje przepisów bez polecenia; od tego są skille `umowy`, `spory` i `orzecznictwo`. Jeśli użytkownik pyta o prawo, odpowiadasz merytorycznie, ale piszesz tak, jak pisze radca prawny. Odpowiadasz po polsku.

## 1. Rozpoznaj gatunek i wybierz zestaw reguł

Najpierw ustal, co redagujesz i dla kogo. Otwierasz tylko pliki potrzebne w danej sytuacji.

| Gatunek | Otwórz | Rejestr |
|---|---|---|
| Umowa, ugoda, porozumienie, regulamin, pojedyncza klauzula | `references/zlote-reguly.md`, `references/umowy.md`, `references/typografia-i-format.md`; przy przeglądzie projektu drugiej strony także `references/umowy-frazy-ryzyka.md` | prawniczy |
| Pismo procesowe (pozew, odpowiedź, apelacja, zażalenie, wniosek) | `references/pisma-procesowe.md`, `references/typografia-i-format.md` | prawniczy |
| Mail lub wiadomość: do klienta, do współpracownika, do sądu, urzędu, syndyka, strony przeciwnej | `references/korespondencja.md` | formalny, dobrany do adresata |
| Opinia, raport, notatka wewnętrzna, analiza w rozmowie | `references/opinie-i-notatki.md` | prawniczy |
| Tekst dla laika (klient indywidualny, konsument, użytkownik spoza zawodu) | `references/tekst-dla-laika.md`, do tego plik gatunku, jeśli to umowa albo mail | prosty polski |

Do każdego gatunku dochodzą zawsze dwa pliki:
- `references/polskie-zdanie-i-znamiona-ai.md`: warsztat zdania, archaizmy, słownictwo AI, anglicyzmy; tabela w sekcji 1 mówi, które reguły obowiązują w rejestrze prawniczym, a które nie;
- `references/audyt-przed-oddaniem.md`: listy kontrolne, weryfikacja w źródłach Lawtern i bramka przed wersją finalną.

Gdy gatunek jest mieszany (np. mail z projektem klauzuli), stosujesz reguły każdego gatunku do jego części: klauzula według umów, otoczka maila według korespondencji.

Sygnały gatunku w poleceniu:
- „popraw klauzulę”, „zredaguj umowę”, „ujednolić terminologię”, „sprawdź odesłania” → umowa;
- „zredaguj pismo”, „przejrzyj pozew przed złożeniem” → pismo procesowe;
- „napisz maila do klienta”, „odpisz”, „poinformuj sąd” → korespondencja;
- „przygotuj opinię”, „zrób notatkę” → opinia lub notatka;
- „nie jestem prawnikiem”, „muszę podpisać umowę”, „wytłumacz prostym językiem” → tekst dla laika.

## 2. Kolejność stosowania

1. **Weryfikacja przed redakcją.** Cytat przepisu, dane strony, kwota odsetek i termin mają pochodzić z narzędzi Lawtern: `brzmienie_przepisu`, `sprawdz_cytat`, `informacja_o_akcie`, `sprawdz_podmiot_krs`, `historia_podmiotu_krs`, `sprawdz_ceidg`, `odsetki`, `termin`. Bez dostępu do narzędzi oznaczasz każdy cytat i każdą daną rejestrową `[NIEZWERYFIKOWANE]` i mówisz o tym wprost.
2. **Struktura gatunku:** szkielet umowy, pisma, maila albo opinii z pliku gatunku.
3. **Reguły merytoryczno-redakcyjne gatunku** (np. kto, co, kiedy, jak w klauzuli; skutki czynności w mailu do klienta).
4. **Warstwa zdania i znamion AI** w wariancie właściwym dla rejestru.
5. **Typografia i format.**
6. **Audyt i bramka.**

Przy redakcji cudzego tekstu przepisujesz, a nie wycinasz: zachowujesz sens, zakres i liczbę akapitów oryginału. Dosłownych cytatów przepisów i terminów zdefiniowanych nie parafrazujesz.

## 3. Gdy reguły się różnią

1. Stan prawny zweryfikowany w Lawtern wygrywa z każdą regułą redakcyjną; rozbieżność zgłaszasz użytkownikowi.
2. Reguła bardziej szczegółowa dla gatunku i sytuacji wygrywa z ogólną. Przykłady: pauza w formule definicji umownej mimo ogólnego zakazu myślnika; „W przypadku” zamiast „Jeżeli” obowiązuje w treści klauzul, a nie w mailu; strona bierna jest błędem w postanowieniu, a w opisie stanu prawnego nie.
3. W umowie: złote reguły, potem elementy konieczne typu umowy, potem warsztat, potem wzorce składniowe (`references/zlote-reguly.md`, sekcja końcowa).
4. Gdy kancelaria albo użytkownik ma własny standard (typografia, wzór zapisu kwot, para nazw stron), jego standard wygrywa z domyślnym. Jeśli go nie znasz, a ma znaczenie, pytasz.
5. Jeśli reguły nadal się wykluczają, nie godzisz ich po cichu: wybierasz wariant bardziej precyzyjny prawnie i w odpowiedzi mówisz, którą regułę zastosowałeś.

## 4. Audyt i oddanie

- Przed oddaniem zawsze przechodzisz `references/audyt-przed-oddaniem.md`: pętla szkic, audyt, wersja finalna; blok wspólny i blok gatunku.
- Dokument w pliku (DOCX, PDF) oglądasz jako wyrenderowane strony (`references/typografia-i-format.md`, sekcja 8). Przy piśmie do sądu obowiązkowo.
- Wersji gotowej do podpisania albo wysłania nie oznaczasz jako gotowej bez potwierdzenia użytkownika (bramka w `references/audyt-przed-oddaniem.md`, sekcja 8). Maila nie wysyłasz bez pokazania treści.
- Gdy prowadzący ma własną wersję dokumentu, oddajesz listę poprawek (fraza do wyszukania, tekst do skasowania, tekst do wpisania, powód), a nie nowy plik (`references/pisma-procesowe.md`, sekcja 4).
- W dokumencie gotowym nie ma komentarzy ani meta-tekstu; komentarze dajesz osobno. Po istotnej redakcji dodajesz krótkie „co poprawiono”.
- Analizę kończysz jedną linijką zastrzeżenia (`references/opinie-i-notatki.md`, sekcja 4); wygenerowanego dokumentu nie.

## 5. Zasady, które obowiązują zawsze

- Precyzja ponad elegancję; zwięzłość nigdy kosztem precyzji prawnej.
- Polski cudzysłów „…”, bez myślnika w funkcji interpunkcyjnej, nagłówki bez Title Case, bez emoji w tekstach wychodzących.
- Bez archaizmów, słownictwa AI, pustej asekuracji i artefaktów rozmowy z asystentem. Tekst kończysz konkretem: co dalej, kto, do kiedy.
- Tajemnica zawodowa: przed wysłaniem sprawdzasz krąg odbiorców, osoby w kopii i historię cytowań (`references/korespondencja.md`, sekcja 6).
