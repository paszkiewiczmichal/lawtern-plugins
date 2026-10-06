# Opinie, raporty i notatki

Opinia prawna, raport (np. due diligence), notatka wewnętrzna, analiza dla użytkownika w rozmowie. Język: rejestr prawniczy z `polskie-zdanie-i-znamiona-ai.md`.

## 1. Struktura

Kolejność: teza, stan faktyczny, analiza, wnioski.

1. **Teza:** jedno zdanie, co ustalono albo co się rekomenduje.
2. **Stan faktyczny:** tylko fakty istotne dla analizy.
3. **Podstawa prawna:** przepisy i orzecznictwo, bez parafrazowania. Brzmienie przepisu sprawdzasz narzędziem `brzmienie_przepisu`, cytat narzędziem `sprawdz_cytat`; powołane orzeczenia według skilla `orzecznictwo`. Bez narzędzia: `[NIEZWERYFIKOWANE]` przy każdym cytacie i powiedz o tym wprost.
4. **Analiza:** zastosowanie prawa do faktów.
5. **Wnioski i rekomendacje:** co zrobić, kto i w jakim terminie.

Nie piszesz wstępu wyjaśniającego, po co jest raport (tytuł to wyjaśnia), ani zakończenia w rodzaju „mam nadzieję, że to pomoże”.

## 2. Czego nie piszesz

- „W ramach niniejszego opracowania postaramy się…”
- „Jak wynika z powyższego…”
- „Reasumując powyższe wywody…”
- „Należy podkreślić, że…”
- zdań, które nie wnoszą treści do analizy.

Asekurację zostawiasz tylko uzasadnioną merytorycznie (rozbieżne poglądy, rozbieżne orzecznictwo, realna niepewność wyniku). Łacina jest dopuszczalna w analizie i komentarzu, gdy jest naprawdę potrzebna, nie dla popisu.

## 3. Przykład: wstęp raportu

**PRZED:**
> Niniejszy raport ma na celu przedstawienie analizy prawnej dotyczącej kluczowych kwestii związanych z przedmiotową transakcją. W ramach poniższego opracowania postaramy się w sposób holistyczny omówić najważniejsze aspekty prawne, które wymagają szczególnej uwagi w kontekście planowanego nabycia udziałów.

**PO:**
> Transakcja nabycia 100% udziałów w spółce X Sp. z o.o. wymaga uprzedniego uregulowania trzech kwestii: (1) zgody UOKiK na koncentrację, (2) wyjaśnienia statusu prawnego nieruchomości przy ul. Długiej 1 w Gdańsku, (3) zwolnienia hipoteki przymusowej wpisanej na rzecz Banku Y S.A.
>
> Poniżej przedstawiam analizę każdej z tych kwestii wraz z rekomendowanymi działaniami i terminami.

## 4. Analiza dla użytkownika w rozmowie

To robocza odpowiedź w czacie, a nie dokument wychodzący. Dlatego obowiązują tu odrębne konwencje:
- **Analiza:** Markdown z nagłówkami sekcji; dopuszczalne znaczniki statusu ✅ OK, ⚠️ uwaga, ❌ problem.
- **Audyt ryzyk:** każde ryzyko z poziomem 🔴 KRYTYCZNY, 🟠 WYSOKI, 🟡 ŚREDNI albo 🟢 NISKI, z lokalizacją (§) i rekomendacją.
- **Pojedyncza klauzula:** tekst klauzuli, krótkie uzasadnienie wyboru, ewentualne warianty.
- **Wygenerowany dokument:** gotowy tekst bez komentarzy w treści; komentarze osobno, przed albo po. W wersji finalnej zero meta-tekstu.
- **Zastrzeżenie:** na końcu każdej analizy (nie przy wygenerowanym dokumencie) jedna linijka, raz:

> *Analiza ma charakter pomocniczy i nie zastępuje oceny radcy prawnego prowadzącego sprawę.*

Emoji ze znaczników nie przenosisz do dokumentu, maila ani pisma wychodzącego do klienta, sądu albo kontrahenta.

## 5. Notatka wewnętrzna

Ta sama kolejność (teza, fakty, analiza, wnioski), krócej. Priorytet i termin wprost, jak w wiadomości do współpracownika (`korespondencja.md`, sekcja 4). Przekazując notatkę w zespole, sprawdzasz krąg odbiorców jak przy korespondencji (`korespondencja.md`, sekcja 6).
