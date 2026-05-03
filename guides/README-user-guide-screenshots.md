# User guide screenshots

`HealthDM-User-Guide.html` embeds **inline SVG** placeholders in each figure so images show even when you open the file as `file://` (relative `<img src="screenshots/…">` often fails in that mode).

The `screenshots/*.svg` files in this folder are optional mirrors for reuse; the guide does not depend on them at runtime.

To use real raster screenshots:

1. Run the app (e.g. production stack or local dev) and sign in as needed.
2. Capture each area listed below (recommended width **1280–1440px**, PNG or WebP).
3. Save under `screenshots/`, e.g. `01-cortex-overview.png`.
4. In `HealthDM-User-Guide.html`, replace the matching `<svg>…</svg>` block inside that figure with `<img src="screenshots/01-cortex-overview.png" alt="…" width="960" />` (keep the same `<figcaption>`).

| File | Capture this screen |
|------|---------------------|
| `01-cortex-overview` | `/insights/cortex` — category grid, toolbar (run assessment / refresh / export). |
| `02-dashboard` | `/insights/dashboard` — overview tiles and charts. |
| `03-cortex-category` | `/insights/cortex/<category>` after opening one category — check table + filters. |
| `04-policies-profiles` | `/insights/policies` — uploads list, comparison scores, actions. |
| `05-comprehensive-report` | `/insights/reports/combined` — combined report controls and summary. |
| `06-settings-credentials` | `/settings` — **Cortex Platform Credentials** tab (mask secrets in the image). |

Do **not** commit API keys or customer secrets in screenshots.
