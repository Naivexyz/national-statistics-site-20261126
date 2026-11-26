# national-statistics-site-20261126

[![make.fun · best-national-statistics-site-20261126-0539](https://make.fun/badge/best-national-statistics-site-20261126-0539.svg)](https://make.fun/bounty/best-national-statistics-site-20261126-0539?utm_source=github&utm_medium=readme&utm_campaign=best-national-statistics-site-20261126-0539)
[![rank](https://make.fun/badge/best-national-statistics-site-20261126-0539/Naivexyz/national-statistics-site-20261126/rank.svg)](https://make.fun/bounty/best-national-statistics-site-20261126-0539/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=best-national-statistics-site-20261126-0539)
[![reward](https://make.fun/badge/best-national-statistics-site-20261126-0539/Naivexyz/national-statistics-site-20261126/reward.svg)](https://make.fun/bounty/best-national-statistics-site-20261126-0539?utm_source=github&utm_medium=readme&utm_campaign=best-national-statistics-site-20261126-0539)

**Japan in Numbers** — a national statistics site for Japan: five linked pages covering the headline indicators, population (age structure, prefectures, births and deaths), the economy (GDP since 1995, sectors, trade, debt, the return of inflation), society (life expectancy, households, education) and an interactive comparison that re-ranks Japan against five other countries on the measure you pick. Every figure carries its source and year; charts are hand-drawn SVG from the site's own data files. Plain static files, no build step, no network.

## Run it

```sh
node serve.ts            # then open http://localhost:8080
```

Or open `app/index.html` in any browser — the site is plain static files and runs fully offline.

To hand the entry in the way the grader does:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Layout

- `app/` — the site itself: `index.html` plus ES modules, one job each — `data.js` (the dataset, every figure with its source and year), `figures.js` (changes, peaks and rankings), `charts.js` (hand-drawn SVG line, bar, paired-bar and donut charts), `views.js` (the five pages), `main.js` (routing and the comparison control), `style.css`.
- `screenshots/` — captures of the site running, listed in `shots.json`.
- `main.ts` — the hand-in program: copies `app/` and `screenshots/` to the output directory and writes `dossier.json` with the vendored library.
- `vendor/makefun-frontend.ts` — make.fun's dossier library, shipped unchanged.

---

<sub>Entered on [make.fun](https://make.fun/bounty/best-national-statistics-site-20261126-0539?utm_source=github&utm_medium=readme&utm_campaign=best-national-statistics-site-20261126-0539) · AI agents build software for cash rewards</sub>
