---
name: color-schema
description: "Navrhuje a doporučuje barevná schémata pro UI. Použij vždy při: generování HTML, řešení barev, designu nebo redesignu UI prvků, výběru palety, práci s CSS proměnnými, výběru barev pro světlý nebo tmavý režim."
argument-hint: "Popis požadavku na barevné schéma nebo kontext UI prvku"
---

# Color Schema Skill

## Kdy použít

- Generování nebo úprava HTML/CSS
- Návrh nebo redesign UI prvků
- Výběr barevné palety pro aplikaci
- Řešení kontrastu, přístupnosti nebo konzistence barev
- Přechod mezi světlým a tmavým režimem
- Výběr barev pro kategorie, stav (úspěch/varování/chyba) nebo zvýraznění

## Dostupná schémata

Viz [./references/barvy.md](./references/barvy.md) pro kompletní specifikaci barev, hex hodnot, CSS proměnných a principů.

### Přehled schémat

| Schéma | Primární barva | Vhodné pro |
|--------|---------------|------------|
| **Slate Pro** | Modrá `#2563EB` / `#3B82F6` | Enterprise, B2B nástroje, corporate look |
| **Nordic Teal** | Teal `#0D9488` / `#14B8A6` | Kalendářové/produktivní nástroje, odlišení od generické modré |

## Postup

### 1. Analyzuj požadavek
- Jaký kontext — světlý nebo tmavý režim?
- Jaký charakter aplikace — korporátní, svěží, neutrální?
- Jaké UI prvky jsou řešeny — pozadí, texty, buttony, karty, kategorie?

### 2. Doporuč schéma
Vyber schéma z [./references/barvy.md](./references/barvy.md) na základě:
- **Slate Pro** — pokud je požadována maximální důvěryhodnost, corporate vzhled, nebo srovnání s Jira/GitHub/Outlook
- **Nordic Teal** — pokud je kladen důraz na svěžest, produktivitu nebo odlišení od generické modré; vhodné pro kalendářové aplikace

### 3. Navrhni konkrétní barvy

Vždy používej CSS proměnné z [./references/barvy.md](./references/barvy.md). Příklad struktury:

```css
:root {
  --color-bg: #F8FAFC;
  --color-surface: #FFFFFF;
  --color-text: #0F172A;
  --color-primary: #2563EB;
  /* ... */
}
```

### 4. Zkontroluj přístupnost
- Kontrast text + pozadí musí splňovat **WCAG AA** (min. 4.5:1 pro běžný text, 3:1 pro velký text a UI prvky)
- Nikdy nepoužívej čistou černou `#000000` nebo čistou bílou `#FFFFFF` jako pozadí

### 5. Aplikuj pravidlo 60-30-10
- **60 %** — neutrální pozadí stránky
- **30 %** — sekundární povrchy (karty, sidebar, hlavička)
- **10 %** — akcentní barva (CTA, aktivní prvky, zvýraznění)

## Sdílené principy (platí pro obě schémata)

- Žádná čistá černá ani bílá — vždy jemně odladěné odstíny
- Sémantické barvy jsou stabilní: zelená = úspěch, jantarová = varování, červená = chyba
- Světlý režim jako výchozí, tmavý jako volitelný
- Barvy kategorií událostí: Práce, Osobní, Zdraví & sport, Rodina, Vzdělávání — viz [./references/barvy.md](./references/barvy.md)
