# Kamila Augustyn — strona wizytówka

Strona-wizytówka Kamili Augustyn — 16-krotnej Indywidualnej Mistrzyni Polski w badmintonie i dwukrotnej olimpijki (Pekin 2008, Londyn 2012), dziś związanej z Klubem Badmintona Garnizon w Gdańsku.

## Struktura repozytorium

- **`index.html`** — finalna, jednoplikowa strona (HTML/CSS/JS bez zależności zewnętrznych). To jest wersja do publikacji, np. przez GitHub Pages.
- **`koncepty/`** — trzy warianty projektowe rozważane przed wyborem finalnego kierunku (`koncept-1-smash.html`, `koncept-2-flow.html`, `koncept-3-retro.html`) oraz `koncept-1-smash-kolory.html` z przełącznikiem 10 palet kolorystycznych. Zachowane jako historia procesu projektowego — nie są linkowane z finalnej strony.
- **`artykuly/`**, **`notatki_zrodla.md`** — materiały źródłowe (biogram, wyniki sportowe, dane klubu) użyte do zbudowania treści strony.
- **`img/`** — 9 konkretnych zdjęć faktycznie użytych na stronie (hero + galeria), skopiowanych z `zdjecia/`.
- **`zdjecia/`** (lokalnie, poza repozytorium) — pełny zbiór pobranych miniatur z wyszukiwarki o niepewnej licencji, celowo wykluczony z repo (`.gitignore`) i z historii commitów. Przed podmianą zdjęć w `img/` na docelowe warto pozyskać od klubu materiały w wysokiej rozdzielczości z potwierdzoną zgodą na publikację.

## Panel administracyjny

Strona ma wbudowany panel do samodzielnej edycji przez Kamilę, bez potrzeby znajomości kodu:

- otwiera się ikoną ⚙ w prawym dolnym rogu strony (lub przez dopisanie `#admin` na końcu adresu),
- wymaga PIN-u (do zmiany w panelu — sekcja „Zmiana PIN-u”),
- pozwala edytować **zdjęcie w tle sekcji Hero** (wybór z gotowych zdjęć lub przesłanie własnego — skalowane automatycznie w przeglądarce), **ceny treningów i kortów** oraz **kolorystykę** strony (10 gotowych palet lub własne kolory).

**Ważne ograniczenie:** to zabezpieczenie działa wyłącznie po stronie przeglądarki — dane (ceny, kolory, PIN) zapisują się lokalnie w `localStorage` tej przeglądarki, w której dokonano zmian, a nie globalnie dla wszystkich odwiedzających. Domyślny PIN znajduje się w jawnym tekście w kodzie źródłowym strony (`index.html`), więc każdy, kto obejrzy źródło strony, może go odczytać lub ominąć panel przez konsolę przeglądarki. To wystarcza jako lekka bariera przed przypadkową edycją, ale **nie jest realnym zabezpieczeniem** — nie należy tu trzymać niczego poufnego. Rekomendacja: zmienić domyślny PIN od razu po publikacji. Prawdziwa ochrona i współdzielone zapisywanie zmian między odwiedzającymi wymagałyby prostego backendu (np. mały endpoint API + baza danych) — do dorobienia w razie potrzeby.

## Uruchomienie lokalnie

To statyczna strona bez procesu budowania — wystarczy otworzyć `index.html` w przeglądarce, albo odpalić dowolny lokalny serwer plików, np.:

```
npx serve .
```
