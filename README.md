# Highway Escape

A 3D endless highway racer by AZARR Motors. Weave through traffic at full speed, chain near misses into big combos, grab coins and nitro, and spend your winnings on faster cars.

Built with [Three.js](https://threejs.org/). The game is a single `index.html` plus a local copy of `three.min.js`, so it runs offline.

## Download
Every push to `main` builds fresh downloads. Open the repo's **Releases** page and take the newest release:
- **Android:** `Highway-Escape.apk`. Open it on your phone to install. Android will ask you to allow installing from this source the first time.
- **Windows PC:** `Highway-Escape.exe`. Double-click it and the game opens in its own window, no install needed. Press `F11` for fullscreen. The file is not code-signed, so Windows may show "Windows protected your PC": click **More info**, then **Run anyway**.

You can also open `index.html` in any modern browser.

## Modes
- **One Way:** four lanes of traffic all heading your way. Endless.
- **Two Way:** the left two lanes come at you. Drive on the wrong side for double score.
- **Time Attack:** 60 seconds on the clock; every green checkpoint gantry adds 30 more.

Pick Day, Sunset, Night or Random before each run.

## Scoring
- Every metre scores, and above 100 km/h it scores more: double at 200 km/h, triple at 300.
- **Near miss:** pass close beside a car above 100 km/h. Under a metre to spare is a **Close call**, worth double.
- Near misses in a row build a combo up to x10. It resets after 3 seconds without one.
- Gold coins on the road are worth 5 each. You also earn 1 coin per 250 points at the end of each run.
- Blue canisters refill half your nitro.

## Garage
Eight cars from a free compact hatch to a 400 km/h hypercar. Each one can be upgraded five levels in Engine (top speed and acceleration), Nitro (tank size and refill) and Handling, and repainted in twelve colours.

## Daily goals
Three challenges a day, such as "make 15 near misses in one run" or "reach 280 km/h". Coins are paid the moment you finish one.

## Controls
| Action | Phone | Keyboard |
| --- | --- | --- |
| Steer | ◀ ▶ | `A` `D` or arrow keys |
| Gas | GAS (or turn on Auto accelerate) | `W` / `↑` |
| Brake | BRAKE | `S` / `↓` |
| Nitro | NOS | `Shift` / `Space` |
| Pause | ☰ | `Esc` or `P` |

Settings: sound, music, auto accelerate, high or low graphics, and a far camera. After a crash you can pay coins to continue the same run.

## How the downloads are built
`.github/workflows/build-release.yml` wraps the game with Capacitor for Android and with Electron for Windows (see `desktop/`), then publishes both files as a GitHub release.
