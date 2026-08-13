# EBL — Spin & Win

Interactive prize wheel for Emirates Bespoke Leather (EBL) showroom.
Single self-contained `index.html` — logo is embedded, no build step, no dependencies.
Works as a WordPress/Elementor HTML widget or as a standalone page (e.g. GitHub Pages).

## Use it

Just open `index.html` in a browser, or drop the whole file into an Elementor
**HTML widget**. Spin by tapping or dragging the wheel itself — there's no
separate button. Spinning is unlimited — every spin is a fresh, independent
random draw, with no per-device or per-session restriction.

## Configure (top of the `<script>` in `index.html`)

| Setting | What it does |
|---|---|
| `SEGMENTS` | The 6 prizes, each with a `weight` (odds) and `prize: true/false`. |
| `FORCE_INDEX` | Default forced result (`null` = use odds). |
| `STAFF_PIN` | 4-digit PIN for the staff panel (`""` disables it). |
| `ADMIN_HOLD_MS` | Hold time on the centre wheel logo to open the staff panel. |

## Staff control (per customer)

Hold the **centre wheel logo** for ~1 second → enter the **PIN** → the control panel opens:

- **Next guest wins** — pick the exact prize the next spin lands on (or Random).
- **Gifts available** — toggle any prize off when it's out of stock.

The forced result clears itself after each spin. Press **`R`** any time to
clear the result panel manually.

> Note: the PIN is client-side (fine for a showroom kiosk, but visible in page
> source). For per-customer logging, a winner list, or true access control, a
> small backend is needed.

## Free hosting (GitHub Pages)

Push this repo, then in **Settings → Pages**, set the source to the `main`
branch / root. Your live URL will be `https://<user>.github.io/<repo>/`.
