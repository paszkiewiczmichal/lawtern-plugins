# Złote reguły umowy

Reguły nadrzędne przy redakcji umów, ugód, porozumień i regulaminów. W razie konfliktu mają pierwszeństwo przed `umowy.md` i przed pozostałymi plikami tego skilla, z jednym wyjątkiem: stan prawny zweryfikowany narzędziem Lawtern (`brzmienie_przepisu`, `informacja_o_akcie`) wygrywa z każdą regułą redakcyjną. Rozbieżność zgłaszasz wtedy użytkownikowi.

## Reguła nadrzędna

> Umowa ma jak najlepiej zabezpieczać interes klienta, ale musi być akceptowalna dla drugiej strony.

Klauzulę, która na pewno zostanie odrzucona w negocjacjach (nieograniczona odpowiedzialność kontrahenta, kara w wysokości 100% wartości umowy, zakaz konkurencji na 10 lat bez ekwiwalentu), proponujesz z adnotacją „wariant agresywny” i dajesz obok wariant negocjowalny.

## Reguły kardynalne

1. **Każde pojęcie pisane wielką literą ma definicję** w § Definicje albo przy pierwszym użyciu. Brak definicji to błąd umowy.
2. **Spójna terminologia.** Jedno pojęcie, jeden termin w całym dokumencie. Nie mieszasz „Wykonawca”, „Zleceniobiorca” i „Usługodawca” dla tej samej strony.
3. **Każde odesłanie wewnętrzne** (§ X ust. Y, art. Z) prowadzi do istniejącej jednostki. Po każdej edycji sprawdzasz odesłania.
4. **Brak osieroconych załączników.** Każdy załącznik wymieniony w preambule albo treści istnieje i jest przywołany. Brak załącznika albo brak przywołania to błąd.
5. **Brak powtórzeń.** Jedna regulacja, jedno miejsce w umowie. Klauzuli o karach z § 8 nie powtarzasz w § 12 „Postanowienia końcowe”.
6. **Nigdy nie poświęcasz precyzji prawnej dla zwięzłości.** Zwięzłość jest zaletą, precyzja obowiązkiem.
7. **Elementy konieczne umowy mapujesz przed pracą:** typ umowy, strony, przedmiot, wynagrodzenie, czas. Bez tego nie piszesz ani jednego paragrafu.
8. **Każda umowa ma** datę, miejsce zawarcia i sposób reprezentacji stron z podstawą umocowania (KRS, pełnomocnictwo). Reprezentację sprawdzasz narzędziem `sprawdz_podmiot_krs`, a reprezentację w dacie czynności z przeszłości narzędziem `historia_podmiotu_krs`; przedsiębiorcę jednoosobowego narzędziem `sprawdz_ceidg`.
9. **Klauzule ochronne na korzyść klienta, dla którego pracujesz**, chyba że użytkownik wyraźnie mówi inaczej (np. „piszemy dla drugiej strony, sprawdź, jak nas chronią”).
10. **Język umowy formalny, precyzyjny, zrozumiały; w treści klauzul bez łaciny** („essentialia negotii”, „lucrum cessans”, „dolus”, „culpa”, „ex contractu”). Łacina zostaje w komentarzu i analizie, nie w podpisywanej umowie. Wyjątek: utrwalone polskie sformułowania prawne („siła wyższa”, „z mocy prawa”), gdy ich pominięcie zmienia znaczenie.
11. **Definicje na początku, potem tylko odesłania.** Pojęcie definiujesz raz, na początku umowy: w § Definicje albo w preambule jako „(dalej: „Pojęcie”)”. Dalej używasz wyłącznie zdefiniowanego terminu i nie powtarzasz definicji. Wyjątek: definicja lokalna, gdy pojęcie ma znaczenie tylko w jednym paragrafie (np. „Okres Przejściowy” zdefiniowany w § 2 ugody i używany tylko w § 2–4). Korzyść: zmiana definicji w jednym miejscu działa w całej umowie.
12. **§ 1 to zawsze Przedmiot Umowy** (albo „Przedmiot Ugody”, „Przedmiot Porozumienia”), czyli odpowiedź na pytanie, czym Strony się umawiają, bez szczegółów operacyjnych.
    - Umowa prosta (NDA, cesja, jednorazowe zlecenie, krótka ugoda): § 1 może zawierać komplet zobowiązań i być ostatnim paragrafem merytorycznym przed postanowieniami końcowymi.
    - Umowa złożona (body leasing IT, wdrożenie, umowa ramowa, ugoda kompleksowa): § 1 jest mapą umowy.

      > § 1. Przedmiot Umowy
      > Przedmiotem Umowy jest: 1) [zobowiązanie 1, doprecyzowane w § 2]; 2) [zobowiązanie 2, doprecyzowane w § 3]; 3) [zobowiązanie 3, doprecyzowane w § 4].

    - Błąd: § 1 z terminami, wynagrodzeniem, sankcjami i mechanizmami wykonawczymi, które należą do osobnych paragrafów. § 1 ma być mapą, nie książką.
    - Test: czy osoba, która przeczyta tylko § 1, wie, czym Strony się umawiają?

## Hierarchia przy konflikcie reguł w umowie

1. Stan prawny zweryfikowany w Lawtern.
2. Złote reguły (ten plik).
3. Elementy konieczne danego typu umowy.
4. Warsztat prawnika (`umowy.md`, część A).
5. Wzorce składniowe umowy (`umowy.md`, część B).

---
Część reguł pochodzi z commercial-legal-pl, Kancelaria Radców Prawnych Żurawska Piotrowski i Wspólnicy, Apache 2.0; zmienione.
