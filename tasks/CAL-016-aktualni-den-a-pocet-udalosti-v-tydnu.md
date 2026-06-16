# CAL-016: Aktuální den a počet událostí v týdnu pod seznamem kategorií

**Summary:** Zobrazit pod seznamem kategorií v sidebaru aktuální datum a počet událostí za aktuální týden
**Priorita:** Low
**Story points:** 1
**Labels:** feature, ux

## Popis

Pod seznam kategorií v sidebaru přidat info-panel, který zobrazuje:
- aktuální datum (den, název dne a datum) ve formátu „Pondělí, 16. června 2026"
- počet událostí naplánovaných v aktuálním kalendářním týdnu (pondělí–neděle)

Uživatel tak má vždy po ruce orientaci v čase a rychlý přehled o vytíženosti aktuálního týdne, i když naviguje do jiných týdnů.

## Požadavky

- [ ] Pod `#categoryList` přidat nový element `#sidebarWeekInfo` v `src/index.html`
- [ ] Zobrazit aktuální den – název dne česky + datum (např. „Pondělí, 16. 6. 2026")
- [ ] Zobrazit počet událostí pro **aktuální kalendářní týden** (bez ohledu na zobrazenou navigaci)
- [ ] Počet událostí respektuje aktivní filtry kategorií
- [ ] Panel se aktualizuje při každé změně dat a při přepnutí kategorií
- [ ] Panel zobrazovat vždy (i pokud je počet událostí 0)

## Technické poznámky

- Přidat do `src/index.html` do `<aside class="sidebar">` za `.category-list` nový blok:
  ```html
  <div class="sidebar-week-info" id="sidebarWeekInfo">
      <div class="sidebar-today" id="sidebarToday"></div>
      <div class="sidebar-week-count" id="sidebarWeekCount"></div>
  </div>
  ```
- Cachovat `dom.sidebarToday` a `dom.sidebarWeekCount` v `cacheDomReferences()` v `src/app.js`
- Implementovat funkci `renderSidebarWeekInfo()`:
  - Aktuální datum zjistit z `new Date()` (nikoliv ze stavu navigace)
  - Počet událostí spočítat průchodem `state.events` – filtrovat události spadající do pondělí–neděle aktuálního týdne a respektovat `state.activeCategories`
- Volat `renderSidebarWeekInfo()` z `renderCategories()`, `renderCalendar()`, `renderMonthView()` a ze všech handlerů měnících data nebo kategorie
- Styl `.sidebar-week-info` umístit do `src/styles.css`:
  - oddělit od kategorií horním okrajem (border-top s nízkou průhledností)
  - tmavý semi-transparentní background konzistentní s tématem
  - název dne tučně, datum drobnějším písmem
  - počet událostí zvýrazněn barvou akcentu

## Implementační plán

1. Přidat HTML blok `#sidebarWeekInfo` do `src/index.html` za `.category-list`
2. Přidat CSS styly pro `.sidebar-week-info`, `.sidebar-today`, `.sidebar-week-count` do `src/styles.css`
3. Cachovat nové DOM reference v `cacheDomReferences()` v `src/app.js`
4. Implementovat funkci `renderSidebarWeekInfo()` v `src/app.js`
5. Zavolat `renderSidebarWeekInfo()` na všech relevantních místech

## Akceptační kritéria

- [ ] Pod seznamem kategorií je vidět aktuální den a datum v češtině
- [ ] Je zobrazen počet událostí pro aktuální kalendářní týden
- [ ] Počet respektuje aktivní filtry kategorií
- [ ] Panel se správně aktualizuje po přidání/odebrání události
- [ ] Panel se správně aktualizuje po zapnutí/vypnutí kategorie
- [ ] Vizuální styl je konzistentní s tmavým tématem aplikace
