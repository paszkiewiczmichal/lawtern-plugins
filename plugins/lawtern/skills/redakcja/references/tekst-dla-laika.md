# Tekst dla laika

Gdy odbiorca nie jest prawnikiem: klient indywidualny, konsument, osoba, która „musi podpisać umowę”, student, a także gdy użytkownik skilla sam nie jest prawnikiem.

## 1. Rozpoznaj rolę użytkownika

| Sygnał w wiadomości | Tryb |
|---|---|
| „jestem prawnikiem / radcą / adwokatem”, kontekst kancelarii, profesjonalne pytanie o klauzulę | PRAWNIK (domyślny) |
| „jestem studentem”, „piszę pracę”, „nie jestem prawnikiem”, „pomóż mi zrozumieć”, „muszę podpisać umowę” | LAIK |
| brak sygnałów | PRAWNIK; nie dopytujesz |

**Tryb PRAWNIK:** narzędzie operacyjne, minimum ostrzeżeń, zakładasz wiedzę prawniczą.

**Tryb LAIK:** przy każdym wyniku dodajesz blok:

> ⚠️ **Dla Ciebie jako osoby spoza zawodu prawniczego:** Ten dokument wymaga weryfikacji przez radcę prawnego lub adwokata przed podpisaniem. Nie podpisuj umowy wyłącznie na podstawie analizy AI.

W trybie LAIK nie tworzysz finalnej wersji dokumentu gotowej do podpisania. Tworzysz draft oznaczony `[DRAFT — WYMAGA WERYFIKACJI PRAWNIKA]` na początku i na końcu.

## 2. Język

- Prosty polski; żargon tłumaczysz, skróty prawnicze wyjaśniasz albo pomijasz.
- Pełne zdania, ale bez utraty precyzji.
- Jasno mówisz, co oznacza dany etap sprawy i co z niego wynika dla odbiorcy.
- Skutki czynności, nie sam fakt (`korespondencja.md`, sekcja 4).
- Przy sprawie osobistej (rodzinnej, majątkowej, spadkowej) ton empatyczny; potwierdzasz odbiór wrażliwych materiałów i mówisz, co się z nimi dalej dzieje.
- Wszystkie reguły z `polskie-zdanie-i-znamiona-ai.md` obowiązują w wariancie dla tekstów spoza rejestru prawniczego (tabela w sekcji 1 tamtego pliku). Jeśli użytkownik poda próbkę własnego stylu, kalibrujesz głos według sekcji 8.

## 3. Objaśnienie przy klauzuli

Gdy laik dostaje umowę z klauzulą, której prawdopodobnie nie zrozumie (limit odpowiedzialności, wina umyślna, zwolnienie z odpowiedzialności), możesz dodać ramkę „Wyjaśnienie (charakter informacyjny)”: 2–3 zdania prostym językiem, wizualnie oddzielone od klauzuli. Ramka nie zmienia treści normatywnej (`typografia-i-format.md`, sekcja 7).
