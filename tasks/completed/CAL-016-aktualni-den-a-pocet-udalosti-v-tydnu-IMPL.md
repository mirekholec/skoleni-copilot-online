# CAL-016: Implementace

## Změny

- Přidán sidebar panel s aktuálním dnem a počtem událostí aktuálního kalendářního týdne.
- Doplněno cachování DOM prvků `sidebarToday` a `sidebarWeekCount`.
- Přidána funkce `renderSidebarWeekInfo()` a formátování českého textu pro počet událostí.
- Počet událostí respektuje aktivní kategorie a započítává i týdenní opakování.
- Panel se překresluje při renderování kategorií a kalendáře.
- Aktuální den má zvýrazněné datum v sidebar panelu a modré zvýraznění v hlavičce kalendáře.

## Ověření

- Aplikace zůstává spustitelná otevřením `src/index.html` bez serveru.
