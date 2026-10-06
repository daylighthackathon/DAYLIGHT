# Daylight – Every claim, in the light

## Co to je
Agent pro HR: vloží CV a jméno kandidáta, agent prohledá veřejný internet a ke každému
tvrzení z CV určí stav (ověřeno / částečně / rozpor / neověřitelné) a ukáže zdroj.

## Jak to funguje
Web (daylight.html) → Make.com (webhook) → Apify Google Search Scraper → OpenAI → Make Data store → web.

## Jak to spustit
1. Importovat blueprints/*.json do Make.com a zapnout oba scénáře.
2. Vložit URL webhooků do daylight.html (WEBHOOK_START, WEBHOOK_RESULT).
3. Otevřít daylight.html v prohlížeči.
Bez URL běží web v DEMO režimu (simulace).

## Co funguje
- (vypište po testu)

## Co je simulované nebo chybí
- DEMO režim je simulace.
- Nepokrýváme LinkedIn (omezený přístup).
- Neověřitelné neznamená nepravdivé.
- Shoda identity je odhad.

## Validace
- Testovací sada: 4 případy, X tvrzení, shoda Y %.

## Etika
- Používáme jen veřejné profesní informace, citlivé kategorie filtrujeme.
- Výstup je podklad pro člověka, nerozhoduje o kandidátovi.
