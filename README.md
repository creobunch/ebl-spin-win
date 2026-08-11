# EBL — Spin & Win

Interactive prize wheel for Emirates Bespoke Leather (EBL) showroom.
Single self-contained `index.html` — logo is embedded, no build step, no dependencies.
Works as a WordPress/Elementor HTML widget or as a standalone page (e.g. GitHub Pages).

## Use it

Just open `index.html` in a browser, or drop the whole file into an Elementor
**HTML widget**. Spin by tapping the button, or tapping / dragging the wheel itself.

## Configure (top of the `<script>` in `index.html`)

| Setting | What it does |
|---|---|
| `SEGMENTS` | The 6 prizes, each with a `weight` (odds) and `prize: true/false`. |
| `MODE` | `"kiosk"` = shared showroom tablet, auto-resets for the next guest. `"once"` = one spin per device. `"staff"` = shows a "next guest" reset button. |
| `RESET_AFTER_MS` | Kiosk auto-reset delay (ms). |
| `FORCE_INDEX` | Default forced result (`null` = use odds). |
| `STAFF_PIN` | 4-digit PIN for the staff panel (`""` disables it). |
| `ADMIN_HOLD_MS` | Hold time on the logo to open the staff panel. |

## Staff control (per customer)

Hold the **EBL logo** for ~1 second → enter the **PIN** → the control panel opens:

- **Next guest wins** — pick the exact prize the next spin lands on (or Random).
- **Gifts available** — toggle any prize off when it's out of stock.

After the guest spins, the wheel auto-resets and the forced result clears.
Press **`R`** any time for an instant staff reset.

> Note: the PIN is client-side (fine for a showroom kiosk, but visible in page
> source). For per-customer logging, a winner list, or true access control, a
> small backend is needed.

## Free hosting (GitHub Pages)

Push this repo, then in **Settings → Pages**, set the source to the `main`
branch / root. Your live URL will be `https://<user>.github.io/<repo>/`.
