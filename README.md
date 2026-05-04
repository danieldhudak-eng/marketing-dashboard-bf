# Body & Future — Marketing Dashboard

Samostatná Vite app pre B&F Meta Ads dashboard. Postavená na rovnakej kostre ako STO verzia, prebrandovaná do farieb a typografie Body & Future.

## Spustenie

```bash
cd marketing-dashboard-bf
npm install
npm run dev
```

## Konfigurácia

Po prvom spustení sa otvorí Settings panel:

1. **Meta Access Token** — token z Meta Business / Facebook Developers.
2. **B&F Ad Account ID** — ID účtu Body & Future (napr. `1234567890`, `act_` prefix sa pridá automaticky).
3. **RIO Ad Account ID** — *zatiaľ neaktívne, pripravené na neskoršie pridanie.*
4. **Supabase Database** *(voliteľné)* — pre cloud sync kategórií a tagov.

## Branding

- **Primárna farba:** B&F zelená `#7BC242` (z loga)
- **Paleta grafov:** `#7BC242`, `#8680bf`, `#fcca8d`, `#64ccca`, `#fa8a70`, `#452213`
- **Typografia:** Bebas Neue (headlines) + Baloo 2 (body)
- **Default kategórie:** Kvíz, Mestá Intro, Waldo

## Deploy

Vite `base` je nastavené na `/marketing-dashboard-bf/` — pripravené na GitHub Pages s rovnomenným repozitárom.

## RIO účet

Druhý účet v segmente headera je zamknutý ikonou zámku a označený "V príprave". Po pridaní stačí v `App.jsx`:
- odstrániť `disabled` na `<button>` v `.acct-seg`
- v `fetchData()` odkomentovať vetvu pre `account === 'rio'` (analogicky k SK v STO verzii)
- pridať RIO ID input do Settings (zrušiť `disabled` atribút)
