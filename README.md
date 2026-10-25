# Strona MrDefeat_ – instrukcja

Strona składa się z trzech plików, które muszą leżeć **w jednym folderze**:

| Plik | Do czego służy |
|---|---|
| `index.html` | cała strona (wygląd, teksty, skrypty) |
| `avatar.gif` | Twój awatar w karcie Discorda |
| `og-image.png` | miniatura, którą widać po wklejeniu linku np. na Discordzie |

Nie potrzebujesz żadnych programów. Do edycji wystarczy Notatnik (Windows) albo edytor tekstu w telefonie.

---

## 1. Wgranie strony za darmo (GitHub Pages), także z telefonu

1. Wejdź w przeglądarce na `github.com` (nie w aplikacji, bo w aplikacji nie wgrasz plików) i załóż konto.
2. Kliknij **+ → New repository**.
3. Nazwij repozytorium dokładnie **`twojnick.github.io`** (ze swoim loginem GitHub), ustaw **Public** i utwórz.
4. Wybierz **Add file → Upload files**, wskaż trzy pliki i kliknij **Commit changes**.
5. Po 1–2 minutach strona działa pod `https://twojnick.github.io`.

## 2. Aktualizacja strony

Zmieniony plik wgrywasz tak samo: **Add file → Upload files**, ten sam plik o tej samej nazwie. GitHub zastąpi stary. Zmiana pojawi się po minucie lub dwóch. Jeśli nie widzisz zmian, odśwież stronę z wyczyszczeniem pamięci podręcznej (na komputerze `Ctrl + F5`).

## 3. Miniatura przy udostępnieniu (ważne po wgraniu)

W `index.html` znajdź linię:

```
<meta property="og:image" content="https://TWOJ-NICK.github.io/og-image.png">
```

i zamień `TWOJ-NICK.github.io` na adres swojej strony. Discord zapamiętuje podgląd, więc zmiana może pojawić się z opóźnieniem.

## 4. Gdzie co zmienić w `index.html`

Wszystkie teksty są w dwóch miejscach: po polsku w bloku `pl: {` i po angielsku w bloku `en: {` (w skrypcie na dole pliku). Pozostałe rzeczy zmienisz tak:

- **ID Discorda (status na żywo):** linia `const DISCORD_ID = "...";` na górze skryptu. Żeby karta pokazywała status, musisz być na serwerze Discord **Lanyard** (`discord.gg/lanyard`).
- **Adres serwera Minecraft ze statusem graczy:** linia `const SERVER_ADDRESS = "";` (np. `"mc.twojserwer.pl"`). Dopóki jest pusta, sekcja „Serwer” jest ukryta.
- **Sprzęt:** w sekcji `id="hardware"` każdy wiersz to jeden `<div><dt>…</dt><dd>…</dd></div>`. Skopiuj wiersz, żeby dodać nowy, albo usuń go, żeby usunąć. Nazwę wiersza dopisz też w obu blokach językowych (klucz `data-i18n`).
- **Mail i nick Discorda w kontakcie:** wyszukaj w pliku `business.mrdefeat@gmail.com` i `_mrdefeat_`.
- **Strona Pixalis.pl:** wyszukaj `pixalis.pl`, zmienisz adres linku i teksty w karcie.
- **Awatar:** podmień plik `avatar.gif` na inny o tej samej nazwie.
- **Gry:** w sekcji `id="games"` każda karta to jeden blok `<a class="card" ...>`. Skopiuj go, żeby dodać grę, i zmień adres profilu, literę w ikonie oraz nick. Głowa skina w karcie Minecraft jest pobierana z usługi `mc-heads.net` na podstawie nicku, więc zmień go w adresie obrazka. Używaj zwykłego, publicznego adresu profilu (np. Steam bez końcówki `/edit/info`).

## 5. Własna domena (opcjonalnie)

Adres `twojnick.github.io` jest darmowy i działa bez końca. Jeśli chcesz krótszy, np. `mrdefeat.pl`:

1. Kup domenę u rejestratora. Przed zakupem sprawdź **cenę odnowienia**, a nie tylko pierwszego roku.
2. W repozytorium wejdź w **Settings → Pages → Custom domain** i wpisz domenę.
3. U rejestratora ustaw rekordy DNS według instrukcji, którą GitHub pokaże na tej samej stronie.
4. Po zmianie adresu poprawisz też linię `og:image` z punktu 3.

## 6. Najczęstsze problemy

- **Zamiast awatara widzę literę „M”.** `avatar.gif` leży w innym folderze niż `index.html` albo go nie wgrano.
- **Karta Discorda nie pokazuje statusu.** Dołącz do serwera Lanyard i odśwież stronę.
- **Miniatura się nie wyświetla.** Sprawdź punkt 3 i wklej link jeszcze raz po kilku minutach.
- **Po zmianie nic się nie zmieniło.** Odśwież stronę z wyczyszczeniem pamięci podręcznej (punkt 2).
