# Pisma procesowe

Pozew, odpowiedź na pozew, apelacja, zażalenie, sprzeciw, replika, wniosek. Analiza sprawy i ocena szans należą do skilla `spory`; ten plik dotyczy redakcji i kontroli pisma przed podpisem. Warstwę języka bierzesz z `polskie-zdanie-i-znamiona-ai.md` (rejestr prawniczy), znaki i plik z `typografia-i-format.md`.

## 1. Struktura

Każde pismo procesowe ma obowiązkową strukturę wynikającą z KPC. Nie wymyślasz własnej.

```
[Miejscowość], [data]

[Nazwa sądu]
[Wydział]
[Adres]

Powód: [imię i nazwisko / firma], [adres]
Pozwany: [imię i nazwisko / firma], [adres]

Wartość przedmiotu sporu: [kwota] zł

POZEW O ZAPŁATĘ
(albo odpowiednia nazwa pisma)
```

- Wnioski na początku (czego żądasz), uzasadnienie po nich.
- Twierdzenia faktyczne oddzielone od argumentacji prawnej.
- Każde twierdzenie faktyczne ma dowód (w nawiasie albo jako „Dowód:”).
- Podpis pełnomocnika z numerem wpisu na listę.
- Kwota sporna cyfrą i słownie; data w treści „do dnia 30 czerwca 2026 roku” (`typografia-i-format.md`, sekcja 4).

## 2. Język pisma

- Rzeczowo, bez elementu emocjonalnego i potocznego.
- Strona czynna tam, gdzie chodzi o to, kto co zrobił; strona bierna dopuszczalna w opisie stanu prawnego.
- Bez archaizmów, słownictwa AI, pustej asekuracji i fraz typu „Należy podkreślić, że…”.
- Przepisy cytujesz dosłownie, po sprawdzeniu brzmienia narzędziem `brzmienie_przepisu`, a cytat porównujesz narzędziem `sprawdz_cytat`. Bez narzędzia: przy cytacie dopisujesz `[NIEZWERYFIKOWANE]` i mówisz o tym wprost.
- Terminy procesowe liczysz narzędziem `termin`, odsetki narzędziem `odsetki`, nie w pamięci.

## 3. Audyt merytoryczny przed podpisem

Uruchamiasz na gotowym piśmie, obok kontroli formy (`audyt-przed-oddaniem.md`) i obok sprawdzenia, czy powołane orzeczenia istnieją (skill `orzecznictwo`). Ten audyt pilnuje czegoś trzeciego: czy to, co piszesz, ma pokrycie w materiale sprawy, a nie tylko brzmi przekonująco. Zajmuje kilkanaście minut.

1. **Kwantyfikatory ogólne.** Wyszukaj każde: „żadne”, „żadnego”, „wszystkie”, „jedyne”, „jedynym”, „wyłącznie”, „ani razu”, „nie powołał”, „w całym”, „nigdy”, „zawsze”. Przy każdym pytasz: czy mam pokrycie w stu procentach materiału, którego to dotyczy? Jeśli nie, zawężasz twierdzenie do tego, co wiesz. Zawężone zdanie broni tej samej pozycji, a nie da się go podważyć.
2. **Twierdzenia o piśmie przeciwnika.** Czy przeczytałeś każdą jego stronę? Jeśli nie, każde zdanie typu „Pozwany nie powołał”, „W całym zażaleniu”, „Przeciwnik pomija” jest niezabezpieczone. Odesłania („sekcja III pkt 5–9”, „strona 10”, „przypis 12”) otwierasz i potwierdzasz.
3. **Cytaty.** Każdy fragment w cudzysłowie porównujesz znak po znaku ze źródłem: nie z notatką, nie ze streszczeniem. Sprawdzasz też, czy cytowany fragment stoi w tej części uzasadnienia, o której piszesz; zdanie może być prawdziwe, a jego umiejscowienie fałszywe.
4. **Definicje i tezy doktrynalne z pamięci.** Wyszukaj zdania definiujące („powszechnie znane są fakty, o których…”, „przez interes prawny rozumie się…”). Bez źródła je usuwasz; argument prawie zawsze obejdzie się bez nich. To najczęstsze wejście treści z pamięci modelu.
5. **Liczby.** Przeliczasz każdą: sumy, różnice, przeliczenia walutowe, wartość przedmiotu sporu, liczbę lat. Sprawdzasz, czy liczba znaczy to, co przy niej napisano. „Strona X zapłaciła o Y więcej, niż otrzymała” zakłada więcej (np. że dochodzona kwota wyczerpuje całość spłat) niż „świadczenia dochodzone pozwem przewyższają [bazę] o Y”; druga wersja nie zakłada nic ponad treść pozwu.
6. **Oznaczenie stron.** Czy nazwa strony nie zmieniła się w toku procesu? Starsze dokumenty mogą nosić dawną nazwę; tego nie rozstrzygniesz z samych akt, więc pytasz prowadzącego, a dane rejestrowe sprawdzasz narzędziem `sprawdz_podmiot_krs` (stan na dzień czynności: `historia_podmiotu_krs`; przedsiębiorca jednoosobowy: `sprawdz_ceidg`). Sprawdzasz też sygnatury obu instancji, wydział, adres sądu, dane pełnomocników, PESEL, KRS.
7. **Powołania z drugiej ręki.** Orzeczenie, którego pełnego tekstu nie masz, oznaczasz jako powołane za wskazanym źródłem. Bez tego dopisujesz zastrzeżenie albo usuwasz powołanie.
8. **Twoje tezy a ustalenia sądu.** Wyłapujesz zdania, które brzmią jak cudze ustalenie, a są twoim wnioskiem. Prowadzący musi wiedzieć, które zdania obroni cytatem, a które musi obronić sam.
9. **Warstwa językowa i forma.** `audyt-przed-oddaniem.md`, w tym obowiązkowy przegląd wyrenderowanego pliku (`typografia-i-format.md`, sekcja 8).

## 4. Format zgłoszenia poprawek

Jeśli prowadzący ma własną, poprawioną wersję dokumentu, nie wysyłasz mu nowego pliku. Dajesz listę. Nie piszesz „znalazłem kilka rzeczy”. Dla każdej poprawki podajesz:
- frazę do wyszukania (Ctrl+F),
- dokładny tekst do skasowania,
- dokładny tekst do wpisania,
- jedno zdanie, dlaczego.

Kolejność: najpierw to, co przeciwnik mógłby wytknąć, potem reszta.
