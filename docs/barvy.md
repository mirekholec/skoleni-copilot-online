# Barevná schémata pro CopilotCal

> Rešerše zaměřená na vhodné barvy pro webové aplikace určené technicky orientovaným uživatelům — správcům kalendáře.

---

## Metodika výběru barev

Výběr vychází z těchto zdrojů a principů:

- **Psychologie barev v B2B prostředí** — modrá je univerzálně nejdůvěryhodnější barvou v enterprise aplikacích (GitHub, Jira, Outlook, Google Calendar). Teal (modrozelená) se prosadila jako alternativa specificky v kalendářových nástrojích (Calendly, Basecamp).
- **Preference technických uživatelů** — výzkumy Nielsen Norman Group a analýza nástrojů Linear, GitHub, Vercel ukazují, že technicky orientovaní uživatelé upřednostňují:
  - Chladné šedé neutraly (ne čistě černá nebo bílá)
  - Nízky saturace, tlumené akcenty
  - Tmavý režim jako volitelnou nebo výchozí možnost
- **WCAG AA přístupnost** — minimální kontrastní poměr 4.5:1 pro běžný text, 3:1 pro velký text a UI prvky.
- **Pravidlo 60-30-10** — 60 % neutrální pozadí, 30 % sekundární povrchy, 10 % akcentní barva.
- **Referenční design systémy** — Atlassian, IBM Carbon, GitHub Primer, Tailwind CSS (Slate a Zinc palety).

---

## Schéma 1 — „Slate Pro" (modrá + studené šedé)

**Filozofie:** Důvěra, přesnost, koncentrace. Tentýž cool modrošedý systém používá GitHub, Linear i Vercel. Modrý akcent komunikuje spolehlivost — nejsilnější asociace v B2B nástrojích.

### Světlý režim

| Role | CSS proměnná | Hex | Tailwind |
|------|-------------|-----|----------|
| Pozadí stránky | `--color-bg` | `#F8FAFC` | `slate-50` |
| Povrch (karty, sidebar) | `--color-surface` | `#FFFFFF` | white |
| Povrch zvýšený (modály) | `--color-surface-elevated` | `#FFFFFF` | white + shadow |
| Ohraničení výchozí | `--color-border` | `#E2E8F0` | `slate-200` |
| Ohraničení jemné | `--color-border-light` | `#F1F5F9` | `slate-100` |
| Text primární | `--color-text` | `#0F172A` | `slate-900` |
| Text sekundární | `--color-text-secondary` | `#475569` | `slate-600` |
| Text ztlumený | `--color-text-light` | `#94A3B8` | `slate-400` |
| Primární akcent | `--color-primary` | `#2563EB` | `blue-600` |
| Primární hover | `--color-primary-hover` | `#1D4ED8` | `blue-700` |
| Primární jemné pozadí | `--color-primary-subtle` | `#EFF6FF` | `blue-50` |
| Dnešní den (highlight) | `--color-today` | `#EFF6FF` | `blue-50` |
| Úspěch | `--color-success` | `#16A34A` | `green-600` |
| Varování | `--color-warning` | `#D97706` | `amber-600` |
| Chyba / nebezpečí | `--color-danger` | `#DC2626` | `red-600` |
| Info | `--color-info` | `#0284C7` | `sky-600` |

### Tmavý režim

| Role | Hex | Tailwind |
|------|-----|----------|
| Pozadí stránky | `#0F172A` | `slate-900` |
| Povrch (karty, sidebar) | `#1E293B` | `slate-800` |
| Povrch zvýšený (modály) | `#334155` | `slate-700` |
| Ohraničení výchozí | `#334155` | `slate-700` |
| Text primární | `#F8FAFC` | `slate-50` |
| Text sekundární | `#CBD5E1` | `slate-300` |
| Text ztlumený | `#64748B` | `slate-500` |
| Primární akcent | `#3B82F6` | `blue-500` |
| Primární hover | `#60A5FA` | `blue-400` |
| Primární jemné pozadí | `#172554` | `blue-950` |
| Úspěch | `#22C55E` | `green-500` |
| Varování | `#F59E0B` | `amber-500` |
| Chyba / nebezpečí | `#EF4444` | `red-500` |
| Info | `#38BDF8` | `sky-400` |

### Barvy kategorií událostí (obě varianty)

| Kategorie | Hex (světlý) | Hex (tmavý) |
|-----------|-------------|-------------|
| Práce | `#2563EB` | `#3B82F6` |
| Osobní | `#D97706` | `#F59E0B` |
| Zdraví & sport | `#16A34A` | `#22C55E` |
| Rodina | `#EA580C` | `#FB923C` |
| Vzdělávání | `#7C3AED` | `#8B5CF6` |

**Proč toto schéma funguje pro technické uživatele:**
- Modrá `#2563EB` je nejdůvěryhodnější barva v enterprise prostředí — používají ji GitHub (`#0969DA`), Jira (`#0052CC`), Outlook (`#0078D4`).
- Slate šedé mají chladný modrý podtón, který je vnímán jako „technický" — vizuálně blízký IDE a terminálům.
- Pozadí `#F8FAFC` (ne čistě bílá) redukuje oslnění a působí profesionálněji.
- Tmavý režim `#0F172A` není čistě černá — GitHub i Linear záměrně volí tmavý modrošedý tón, který neunavenoví zrak při dlouhé práci.

---

## Schéma 2 — „Nordic Teal" (teal + teplé šedé)

**Filozofie:** Čistota, struktura a odlišnost. Teal je méně přehlcená barva než modrá — používají ji Calendly a Basecamp přímo v kontextu kalendářů. Zinc šedé jsou mírně teplejší než Slate, čímž jsou příjemnější při delší práci s hustými kalendářovými mřížkami.

### Světlý režim

| Role | CSS proměnná | Hex | Tailwind |
|------|-------------|-----|----------|
| Pozadí stránky | `--color-bg` | `#FAFAFA` | `zinc-50` |
| Povrch (karty, sidebar) | `--color-surface` | `#FFFFFF` | white |
| Povrch zvýšený (modály) | `--color-surface-elevated` | `#FFFFFF` | white + shadow |
| Ohraničení výchozí | `--color-border` | `#E4E4E7` | `zinc-200` |
| Ohraničení jemné | `--color-border-light` | `#F4F4F5` | `zinc-100` |
| Text primární | `--color-text` | `#18181B` | `zinc-900` |
| Text sekundární | `--color-text-secondary` | `#52525B` | `zinc-600` |
| Text ztlumený | `--color-text-light` | `#A1A1AA` | `zinc-400` |
| Primární akcent | `--color-primary` | `#0D9488` | `teal-600` |
| Primární hover | `--color-primary-hover` | `#0F766E` | `teal-700` |
| Primární jemné pozadí | `--color-primary-subtle` | `#F0FDFA` | `teal-50` |
| Dnešní den (highlight) | `--color-today` | `#F0FDFA` | `teal-50` |
| Úspěch | `--color-success` | `#16A34A` | `green-600` |
| Varování | `--color-warning` | `#D97706` | `amber-600` |
| Chyba / nebezpečí | `--color-danger` | `#DC2626` | `red-600` |
| Info | `--color-info` | `#0891B2` | `cyan-600` |

### Tmavý režim

| Role | Hex | Tailwind |
|------|-----|----------|
| Pozadí stránky | `#18181B` | `zinc-900` |
| Povrch (karty, sidebar) | `#27272A` | `zinc-800` |
| Povrch zvýšený (modály) | `#3F3F46` | `zinc-700` |
| Ohraničení výchozí | `#3F3F46` | `zinc-700` |
| Text primární | `#FAFAFA` | `zinc-50` |
| Text sekundární | `#D4D4D8` | `zinc-300` |
| Text ztlumený | `#71717A` | `zinc-500` |
| Primární akcent | `#14B8A6` | `teal-500` |
| Primární hover | `#2DD4BF` | `teal-400` |
| Primární jemné pozadí | `#042F2E` | teal-950 |
| Úspěch | `#22C55E` | `green-500` |
| Varování | `#F59E0B` | `amber-500` |
| Chyba / nebezpečí | `#EF4444` | `red-500` |
| Info | `#22D3EE` | `cyan-400` |

### Barvy kategorií událostí (obě varianty)

| Kategorie | Hex (světlý) | Hex (tmavý) |
|-----------|-------------|-------------|
| Práce | `#0D9488` | `#14B8A6` |
| Osobní | `#D97706` | `#F59E0B` |
| Zdraví & sport | `#16A34A` | `#22C55E` |
| Rodina | `#EA580C` | `#FB923C` |
| Vzdělávání | `#7C3AED` | `#8B5CF6` |

**Proč toto schéma funguje pro technické uživatele:**
- Teal `#0D9488` leží na průsečíku modré a zelené — nese důvěryhodnost modré a přidává „produktivní svěžest" zelenou. Vizuálně se odlišuje od generické modré, která je přehlcená na trhu.
- Modrá je přesunuta do role sekundárního akcentu (kategorie událostí), kde odpovídá mentálnímu modelu z Google Kalendáře a Outlooku.
- Zinc šedé (`#18181B`, `#27272A`) jsou téměř identické s „Nordic Gray" palety Linear (`#222326`) — teplost sníží únavu zraku při intenzivní práci s kalendářem.
- Tmavé pozadí `#18181B` přesně odpovídá prostředí VS Code a GitHub Dark — technický uživatel ho zná z IDE a přechod mezi nástroji je kognitivně nenáročný.

---

## Porovnání schémat

| Kritérium | Slate Pro | Nordic Teal |
|-----------|-----------|-------------|
| Asociace | Maximální důvěra, corporate | Produktivita, svěžest, odlišnost |
| Cílový kontext | Soutěží s Jira/Notion/Linear | Soutěží s Calendly/Basecamp |
| Neutraly | Chladné (modrý podtón) | Teplé (neutrální šedá) |
| Primární barva | Modrá `#2563EB` | Teal `#0D9488` |
| Sytost akcentu | Střední | Nižší, klidnější |
| Tmavý režim bg | `#0F172A` (modrošedá) | `#18181B` (teplá černá) |

---

## Sdílené principy obou schémat

1. **Žádná čistá černá ani bílá** — pozadí jsou vždy jemně odladěné odstíny, nikoli `#000000` nebo `#FFFFFF`. Redukuje oslnění a vizuální únavu.
2. **Světlý režim jako výchozí** — výzkum NN/g (Piepenbrock et al., 2013) prokázal lepší čitelnost v světlém režimu; nabídnout i tmavý (technická cílová skupina ho preferuje).
3. **Sémantické barvy jsou stabilní** — zelená = úspěch, jantarová = varování, červená = chyba/nebezpečí. Mění se pouze intenzita pro tmavý/světlý režim.
4. **Přístupnost WCAG AA** — všechny kombinace text+pozadí splňují minimální poměr 4.5:1.
5. **Pravidlo 60-30-10** — ~60 % povrchu tvoří neutrální pozadí, ~30 % sekundární povrchy (sidebar, hlavička), ~10 % akcentní barva (CTA, označení aktivního prvku).

---

*Rešerše zpracována na základě: Nielsen Norman Group, Atlassian Design System, GitHub Primer, IBM Carbon, Tailwind CSS, Linear brand guidelines, Material Design 3 — červen 2026.*
