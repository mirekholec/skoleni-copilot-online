# CAL-015: Implementace – Indikátor priority na událostech

## Změny

### `src/styles.css`
- Přidány CSS třídy `.priority-low`, `.priority-medium`, `.priority-high` za sekci `.event-block:hover`
- Každá třída nastavuje `border-left: 3px solid <barva>` dle specifikace

### `src/app.js`
- Ve funkci `createEventBlock()` přidáno `block.classList.add('priority-' + event.priority)` pokud je priorita definována
