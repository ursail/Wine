# Little Secret · Weinkeller (GitHub Pages + Sveltia CMS)

- `index.html` – Dashboard (nur Anzeige, iPad-optimiert)
- `admin/` – Sveltia CMS zum Pflegen der Weine (Login über GitHub)
- `data/wines.json` – die Weindaten, werden vom CMS per Commit gespeichert

## Einrichten
1. Alles aus diesem Ordner in das Repository `ursail/Wine` hochladen (Branch `main`).
2. Settings → Pages → „Deploy from a branch“ → `main` / `/ (root)`.
3. Dashboard: https://ursail.github.io/Wine/  ·  Verwaltung: https://ursail.github.io/Wine/admin/

## Login in der Verwaltung
Einfachste Variante ohne Zusatzdienst: Auf GitHub unter Settings → Developer settings →
Fine-grained personal access tokens ein Token nur für `ursail/Wine` mit der Berechtigung
„Contents: Read and write“ erstellen. In `/admin/` „Mit Token anmelden“ wählen und einfügen.
Komfortabler (GitHub-Button): `sveltia-cms-auth` auf Cloudflare Workers deployen und die URL
in `admin/config.yml` bei `base_url` eintragen.

## Datenschutz
GitHub Pages ist öffentlich. Wer die URL kennt, kann `data/wines.json` lesen, auch Preise und
Lieferanten. Schreiben kann nur, wer Schreibrechte im Repo hat.
