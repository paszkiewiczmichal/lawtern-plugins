# Dyscyplina orzecznictwa — trzy stany sygnatury

> Rozwinięcie R1 (`rdzen-ktzr.md`) na orzecznictwo, wspólne dla całej warstwy spornej. Workflow
> odwołują się tu przez numer sekcji zamiast powtarzać treść (R7 — progressive disclosure).
> Otwórz przy każdym workflow, które cytuje albo ocenia orzecznictwo:
> `pismo-odpowiadajace.md`, `przygotowanie-pozwu.md`, `ocena-sporu.md`, `kwestionowanie-argumentacji.md`,
> `podsumowanie-orzeczenia.md`.

## 1. Trzy stany — rozróżnianie ich jest istotą dyscypliny

Każda sygnatura, którą się posługujesz, ma jeden z trzech stanów. Nie wolno ich mylić ani skracać drogi między nimi.

**Stan A — sygnatura, której nie znasz z materiału sprawy.** Nie wolno jej wymyślić. Nigdy. Nie ma wersji miękkiej: „prawdopodobnie istnieje wyrok SN o tej treści" nie jest podstawą do wpisania sygnatury. Trzy wyjścia: opisać tezę bez sygnatury, poprosić prawnika o wyszukanie w Lex, albo poprosić o to zewnętrzne narzędzie orzecznicze, którym kancelaria dysponuje (sekcja 4). Wybór narzędzia należy do prawnika, nie do Ciebie.

**Stan B — sygnatura już użyta w materiale sprawy** (piśmie już złożonym, notatce prawnika, wcześniejszej analizie). Jej *istnienie* jest tym samym potwierdzone — ktoś świadomie ją tam umieścił. Weryfikacji wymaga wyłącznie *treść*: czy teza, którą jej przypisujesz, rzeczywiście z niej wynika. Nie usuwaj takiej sygnatury dlatego, że sam nie umiesz jej sprawdzić — to jest dokładnie przypadek, w którym prosisz o tekst źródłowy zamiast działać samodzielnie.

**Stan C — sygnatura zweryfikowana co do treści.** Masz przed sobą tekst orzeczenia i wiesz, co w nim stoi. Dopiero teraz wolno świadomie zdecydować, jak mocną tezę na nim oprzeć. Stan C ma dwa poziomy, oznaczaj je jawnie w dokumencie:

- **Przeczytane w całości** — cytujesz swobodnie, dosłownie, z sygnaturą (i numerem LEX/OSNC, jeśli dostępny).
- **Znane z relacji innego orzeczenia albo z monografii/komentarza** — nie masz pełnego tekstu, tylko fragment cytowany przez kogoś innego. Powołujesz, ale w dokumencie piszesz wprost, że strona nie dysponuje pełnym tekstem i powołuje je za wskazanym źródłem. Sąd/czytelnik woli jawne zastrzeżenie od przemilczenia — i to nie jest to samo co Stan B: tu nie masz nawet pewności co do pełnej treści, nie tylko co do tego, że ktoś w sprawie już się na nie powołał.

**Twoja własna teza to osobna, czwarta kategoria — nie powołanie.** Gdy piszesz coś, co jest Twoim wnioskiem, a nie cudzym ustaleniem, musi być jasne dla prowadzącego, które zdania obroni cytatem, a które musi obronić sam (patrz też `audyt-przed-drukiem.md` punkt 8).

## 1a. Czego nie robisz

- **Brak trafienia w wyszukiwarce orzeczeń nie dowodzi, że orzeczenie nie istnieje.** Postanowienia w wielu kategoriach spraw (np. w przedmiocie zabezpieczenia) rzadko trafiają do publicznych portali. Nigdy nie sugeruj w piśmie, że przeciwnik zmyślił sygnaturę, jeśli jedyną podstawą jest brak trafienia w wyszukiwarce — to nie jest dowód.
- **Drobnych literówek w cudzych przypisach nie podnosisz** (zła cyfra w dacie, przestawiony numer sygnatury o oczywistym charakterze pomyłki). To wygląda małostkowo i osłabia mocne argumenty stojące obok.

## 2. Czym dysponujesz do weryfikacji treści

| Rodzaj | Narzędzie | Uwaga |
|---|---|---|
| przepis PL/UE | `brzmienie_przepisu` (z `na_dzien`), przed cytatem `sprawdz_cytat` | obowiązkowo, R1. **Uwaga na numerację historyczną:** przepis cytowany w orzeczeniu sprzed lat może dziś mieć inny numer paragrafu po nowelizacji — nie przepisuj numeracji z cudzego uzasadnienia bez sprawdzenia aktualnej. |
| decyzje organów i interpretacje podatkowe (UOKiK, PUODO, KNF, Dyrektor KIS od 2020 r.) | `szukaj_decyzji` (`organ`), `pobierz_decyzje` | decyzja PUODO nieprawomocna (`nonfinal`) albo uchylona (`repealed`) nie jest ostateczna; interpretacja indywidualna chroni wyłącznie wnioskodawcę - przy innym stanie faktycznym to tylko wskazówka |
| wyrok TSUE | `sprawdz_orzeczenie_tsue(celex)` albo `pobierz_orzeczenie` po sygnaturze `C-…/…`; sentencja: `koniec=true` | CELEX: format `6`+rok+`CJ`+numer, np. `62019CJ0224`. **Czytaj precyzyjnie, który to głos:** punkt, w którym Trybunał *odnotowuje stanowisko sądu odsyłającego albo strony* („sąd odsyłający i rząd X uważają, że…"), to nie jest teza samego Trybunału — dopiero rozstrzygnięcie w dalszej części punktów jest. Pomylenie tych dwóch to częsty błąd przy szybkim czytaniu. |
| orzecznictwo krajowe (SN, sądy powszechne, TK, KIO, NSA, WSA od 2020 r.) | `szukaj_orzeczen` (zawężenie `sad_typ`: m.in. `NSA`, `WSA`), `pobierz_orzeczenie`, `sprawdz_sygnatury` | korpus nie jest kompletny; uchwała NSA wiąże składy sądów administracyjnych (art. 269 § 1 p.p.s.a.); przy braku trafienia: plik źródłowy od prawnika albo zewnętrzne narzędzie (sekcja 4) |

Luka w korpusie (np. brak orzeczenia w bazie) jest realnym ograniczeniem, nie niedopatrzeniem. Praktyczne wyjście: poproś prawnika o wrzucenie tekstów z Lex do rozmowy — kilka plików .docx albo PDF rozwiązuje sprawę na całą sesję.

## 3. Gdy PDF z portalu orzeczeń nie daje się skopiować

Portale sądowe bywają zabezpieczone przed maszynowym odczytem — czcionki Type 3 bez mapowania Unicode. `pdftotext` zwraca wtedy śmieci. Diagnoza: `pdffonts plik.pdf` pokaże typ czcionek. Obejście: renderuj strony i przepuść przez OCR.

```
pdftoppm -jpeg -r 150 plik.pdf strona
tesseract strona-01.jpg - -l pol --psm 6
```

Pakiet `tesseract-ocr-pol` instaluje się przez `apt-get install -y tesseract-ocr-pol`. Przy dokumencie kilkudziesięciostronicowym rozbij OCR na partie — całość w jednej komendzie potrafi przekroczyć limit czasu.

**Alternatywa bez OCR, gdy pracujesz w środowisku z odczytem obrazów:** wyrenderuj strony (`pdftoppm`) i odczytaj każdą narzędziem do odczytu obrazu wprost, zamiast przepuszczać przez `tesseract` do tekstu. Omija błędy rozpoznawania znaków przy trudnej czcionce czy złej jakości skanu — kosztem tego, że **musisz odczytać każdą stronę, bez pomijania żadnej**. Pominięcie choćby jednej strony bywa kosztowne: listy zarzutów czy kluczowe fragmenty rzadko siedzą tam, gdzie by się intuicyjnie oczekiwało (np. nie zawsze na pierwszej stronie) — nie wnioskuj o zawartości pominiętej strony ze struktury dokumentu, zawsze odczytaj literalnie.

**Gdy zweryfikowana teza okazuje się mocniejsza niż to, jak ją dotąd cytowano** — nie przeredagowuj po cichu. Pokaż prawnikowi różnicę: co dokument mówi dziś, co orzeczenie mówi naprawdę, jaki argument to otwiera. Decyzja o wzmocnieniu należy do niego.

## 4. Cross-check przez zewnętrzne narzędzie orzecznicze

Gdy kancelaria dysponuje zewnętrznym narzędziem orzeczniczym (Libra.ai lub inne), warto przepuścić przez nie gotowy dokument. Nie po to, żeby potwierdziło to, co już wiesz — po to, żeby spróbowało znaleźć błąd.

Zapytanie zbuduj tak:

- **Pełny tekst uzasadnienia**, nie streszczenie. Bez nagłówka z danymi osobowymi klienta — PESEL i adresy nie są potrzebne do weryfikacji tez prawnych, a wychodzą do zewnętrznego dostawcy. Sprawdź też, czy z tym dostawcą jest podpisana umowa powierzenia przetwarzania.
- **Konkretne pytania**, nie „sprawdź to": czy przywołane tezy odpowiadają treści orzeczeń, czy jest nowsze orzecznictwo w tym kierunku, czy fragmenty dokumentu nie są ze sobą sprzeczne (sekcja 5), jaki kontrargument może podnieść przeciwnik.
- **Prośbę o pełne sygnatury** przy każdej odpowiedzi, żeby dało się je zweryfikować źródłowo przed wykorzystaniem.

**Odpowiedzi nie przyjmuj na słowo.** Zewnętrzne narzędzie też się myli — bywa, że skraca tekst, gubi po drodze cytowania i zastępuje je gołosłownym „sądy przyjmują", albo przywraca fragmenty, które prawnik wcześniej kazał usunąć. Każdą wskazaną niezgodność sprawdź w tekście źródłowym orzeczenia, zanim cokolwiek zmienisz. Przy scalaniu poprawek porównaj wersje akapit po akapicie i wypisz prawnikowi, co zniknęło.

## 5. Kontrola spójności między cytowanymi orzeczeniami

**Zawsze, gdy dokument cytuje więcej niż jedno orzeczenie.** Przeczytaj całość jednym ciągiem i sprawdź, czy dwa cytowane orzeczenia nie mówią rzeczy przeciwnych. Ryzyko jest realne: różne sekcje powstają w różnych momentach pracy, każda z osobna wygląda dobrze, a razem dają przeciwnikowi gotowy kontrargument z własnego dokumentu.

Przykład z praktyki: pismo twierdziło w jednej sekcji, że ewentualny zarzut potrącenia jest nieskuteczny (za wyrokiem SA Warszawa), a w drugiej cytowało wyrok SA Poznań, który ewentualny zarzut wprost dopuszcza, o ile samo oświadczenie o potrąceniu jest bezwarunkowe. Oba cytaty były prawdziwe. Razem były wpadką.

Wyjścia z takiej kolizji, w kolejności od najlepszego:

- **Odróżnij wprost.** Najmocniejsze rozwiązanie: pokaż, dlaczego drugie orzeczenie dotyczy innego stanu faktycznego. Kolizja zamienia się w precyzję.
- **Zwęź własną tezę** do zakresu, w którym oba orzeczenia się zgadzają.
- **Zrezygnuj ze słabszego argumentu** — zwykle tego opartego na orzeczeniu odosobnionym.

Sprawdź przy okazji, czy orzeczenie, na którym opierasz argument, nie jest tezą mniejszościową — uzasadnienia bywają szczere, skład potrafi napisać, że odstępuje od przeważającego kierunku. I czy stan faktyczny orzeczenia rzeczywiście przystaje do sprawy: wyrok sądu apelacyjnego w sprawie o pożyczkę prywatną waży mniej w sporze frankowym niż wyrok w sprawie frankowej — podobieństwo stanu faktycznego jest częścią siły argumentu, nie tylko sygnatura.

## Powiązane

- `rdzen-ktzr.md` R1, R2 (stopka wersji roboczej), R11 (walidacja cytatu z dokumentu)
- `references/format-checklist.md` — kontrola pliku wyjściowego (finalny render dokumentu, nie tylko tekst)
- `references/audyt-przed-drukiem.md` — czy twierdzenia w gotowym piśmie mają pełne pokrycie w materiale (inny rodzaj kontroli niż to, czy sygnatura jest prawdziwa)
