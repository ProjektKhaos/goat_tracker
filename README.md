# Goat Tracker

En offline-app i en fil för att följa när varje get senast klipptes.

## Vad appen gör
- Låter dig lägga till getter med `namn` och `senast klippt` (datum).
- Räknar automatiskt antal dagar sedan senaste klövklipp.
- Visar status med badge-färger:
  - `0-29 dagar`: grön
  - `30-59 dagar`: orange
  - `60+ dagar`: röd
- Sorterar listan (standard: flest dagar först) och kan växlas till färskast först.
- Sökfilter på namn.
- Snabbåtgärder per get:
  - `Reset idag`
  - ändra namn
  - ändra datum
  - ta bort

## Lagring
All data sparas lokalt i webbläsaren via `localStorage`.

Nycklar som används:
- `goat_tracker_v1_goats`: lista med getter
- `goat_tracker_v1_sort_desc`: sorteringsval (`true/false`)

Det innebär:
- Appen fungerar utan server och utan internet.
- Data följer webbläsaren/enheten, inte ditt konto.

## Export och import
- `Export JSON`: skapar backup i JSON-format (kan kopieras eller laddas ner).
- `Import JSON`: ersätter hela nuvarande listan.

Importerade format som stöds:
- en full payload med `goats`-array
- eller direkt en array med getter

Varje get måste ha giltigt:
- `name` (text)
- `last` i format `YYYY-MM-DD`

## Snabbstart
1. Öppna `goat_tracker.html` i valfri modern webbläsare.
2. Lägg till en get med namn och datum.
3. Använd sök/sortering och knappen `Reset idag` vid behov.
4. Exportera JSON regelbundet för backup.

## Filstruktur
- `goat_tracker.html`: hela appen (HTML, CSS, JavaScript i samma fil)

## Tekniskt
- Ingen backend.
- Ingen databas.
- Ingen extern dependency.
- All logik körs i klienten (browser).

## Licens
MIT License. Se LICENSE för full text.

